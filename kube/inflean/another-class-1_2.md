## 섹션4-12강.

#### 설치 주소
 - Windows: https://cafe.naver.com/kubeops/21
 - Mac : https://cafe.naver.com/kubeops/91
 
 
#### 접속 정보
 - 192.168.56.30
 - root / vagrant

#### Pod 확인
 - k get pods -A
 - Dashboard-Metrics Pending 상태 지속 문제 해결(Vagrantfile 파일 주석처리 되어 있음 : 144 Line)
   - [8-4] Master에 Pod를 생성 할수 있도록 설정
     - kubectl taint nodes k8s-master node-role.kubernetes.io/control-plane- 
   - https://www.inflearn.com/community/questions/1393510/dashboard-metrics-pending-%EC%83%81%ED%83%9C-%EC%A7%80%EC%86%8D

#### 타임존 설정 확인
 - timedatectl

#### 방화벽 해제
 - systemctl stop firewalld OR systemctl disable firewalld
 - ﻿systemctl status firewalld

#### Dashboard
 - https://192.168.56.30:30000/#/login
 
#### Pod 설명, 로그 보기
 - kubectl describe pod &lt;pod-name&gt; -n &lt;name-space&gt;
 - kubectl logs &lt;pod-name&gt; -n &lt;name-space&gt;


## 섹션5-20강. 모니터링 설치 - Loki-Stack (💻 실습포함)
 - 실습 자료실 : https://cafe.naver.com/kubeops/30

#### Grafana 접속
 - 접속 URL : http://192.168.56.30:30001
 - 로그인 :​ id: admin, pw: admin(최초) -&gt; grafana(변경)

#### Grafana Dashboard 모음
 - https://grafana.com/grafana/dashboards/
 - Copy ID to clipboard &gt; import dashboard &gt; import via grafana.com [Load]
 
#### 쿠버네티스 대시보드에 App 배포 실습
 - https://cafe.naver.com/kubeops/31
 
 
 - dashboard 접속 > Namespace [default] > [+] 버튼 > [입력을 통해 생성] > yaml 내용 붙여넣기 > 업로드
    ```yaml
    apiVersion: apps/v1
    kind: Deployment
    metadata:
      name: app-1-2-2-1
    spec:
      selector:
        matchLabels:
          app: '1.2.2.1'
      replicas: 2
      strategy:
        type: RollingUpdate
      template:
        metadata:
          labels:
            app: '1.2.2.1'
        spec:
          containers:
            - name: app-1-2-2-1
              image: 1pro/app
              imagePullPolicy: Always
              ports:
                - name: http
                  containerPort: 8080
              startupProbe:
                httpGet:
                  path: "/ready"
                  port: http
                failureThreshold: 1000
              livenessProbe:
                httpGet:
                  path: "/ready"
                  port: http
              readinessProbe:
                httpGet:
                  path: "/ready"
                  port: http
              resources:
                requests:
                  memory: "100Mi"
                  cpu: "100m"
                limits:
                  memory: "200Mi"
                  cpu: "200m"
    ---
    apiVersion: v1
    kind: Service
    metadata:
      name: app-1-2-2-1
    spec:
      selector:
        app: '1.2.2.1'
      ports:
        - port: 8080
          targetPort: 8080
          nodePort: 31221
      type: NodePort
    ---
    apiVersion: autoscaling/v2
    kind: HorizontalPodAutoscaler
    metadata:
      name: app-1-2-2-1
    spec:
      scaleTargetRef:
        apiVersion: apps/v1
        kind: Deployment
        name: app-1-2-2-1
      minReplicas: 2
      maxReplicas: 4
      metrics:
        - type: Resource
          resource:
            name: cpu
            target:
              type: Utilization
              averageUtilization: 40
	```
 
 - connection refused 문제
    ```
    Warning Unhealthy 2m46s (x25 over 7m46s) kubelet Startup probe failed: Get "http://20.96.235.214:8080/ready": dial tcp 20.96.235.214:8080: connect: connection refused
	```
   - Deployment 스펙에 failureThreshold 값을 100 또는 더 크게.
     - failureThreshold: 10 => failureThreshold: 100
 - App에 지속적으로 트래픽 보내기 (Traffic Routing 테스트)
   - while true; do curl http://192.168.56.30:31221/hostname; sleep 2; echo '';  done;
 - App에 Memory Leak 나게 하기 (Self-Healing 테스트)
   - url 192.168.56.30:31221/memory-leak
 - App에 부하주기 (AutoScaling 테스트)
   - curl 192.168.56.30:31221/cpu-load
 - App 이미지 업데이트 (RollingUpdate 테스트)
   - Namespace: default &gt; 디플로이먼트 &gt; ... &gt; 편집
   ```
    spec:
         containers:
            - name: app-1-2-2-1
              image: 1pro/app-update  # 수정
    ```
   - kubectl 명령으로 할 경우
     - kubectl set image -n default deployment/app-1-2-2-1 app-1-2-2-1=1pro/app-update
 - 기동되지 않는 App 업데이트 (RollingUpdate 테스트)	 
   - Namespace: default &gt; 디플로이먼트 &gt; ... &gt; 편집
   ```
	spec:
		  containers:
			- name: app-1-2-2-1
			  image: 1pro/app-error   # 수정
    ```
   - kubectl 명령으로 할 경우
     - kubectl set image -n default deployment/app-1-2-2-1 app-1-2-2-1=1pro/app-error
   - kubectl 명령으로 업데이트 중지하고 롤백 할 경우
     - kubectl rollout undo -n default deployment/app-1-2-2-1

 - 강의에서 배포한 Object 삭제
   - kubectl delete -n default deploy app-1-2-2-1
   - kubectl delete -n default svc app-1-2-2-1
   - kubectl delete -n default hpa app-1-2-2-1

 
2026년 전자정부 표준프레임워크 컨트리뷰션 기념품 발송 안내] ※응답기한 ~9월30일까지

@bada-egov 님, 안녕하세요.
전자정부 표준프레임워크 센터입니다.
2026년 5월 18일부터 전자정부 서비스 개발 표준 기반인 "전자정부 표준프레임워크"에 민간 및 SW 개발자 등 실 수요자의 아이디어와 다양한 의견을 반영하기 위해 "2026 전자정부 표준프레임워크 컨트리뷰션"을 개최 하였습니다.
표준프레임워크 깃허브(github.com/egovframework)에 기여해주신 귀하의 의견에 감사드리며, 앞으로 전자정부 표준프레임워크 운영·개선 과정에서 유용하게 활용토록 하겠습니다.
본 설문을 작성해 주시면 감사장과 기념품을 발송 드릴 예정이오니, '26년 9월 30일까지 아래의 URL을 통해 설문지로 이동, 항목에 응답 부탁드립니다.(※ 감사장은 실물 배송 원하는 경우만 발송)

↓응답 작성하기(Google 설문지)↓
https://forms.gle/fVTu2GZg9BVqvNfL7

❒ 컨트리뷰션 종료 후, 시상 관련하여 연락 갈 예정이오니, 꼭 통화 가능한 본인 번호를 기재해 주시기 바랍니다.
❒ 귀하께서 답변해 주시는 내용은 컨트리뷰션 참가 확인 및 기념품 발송 목적으로만 활용되며, 제출된 개인정보는 기념품 발송 후 즉시 영구 삭제 처리 됩니다.
❒ 대학(원)생 참여의 경우 재학 중인 학교명 기재 필요.

감사합니다.