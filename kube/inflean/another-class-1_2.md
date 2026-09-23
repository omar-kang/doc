## 섹션4-12강.

#### 설치 주소
 - Windows: https://cafe.naver.com/kubeops/21
 - Mac : https://cafe.naver.com/kubeops/91

 - 섹션3-9강. [무게감 있게 설치하는 방법 0-Windows빠른설치 _ 네이버 카페.pdf](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/%EB%AC%B4%EA%B2%8C%EA%B0%90%20%EC%9E%88%EA%B2%8C%20%EC%84%A4%EC%B9%98%ED%95%98%EB%8A%94%20%EB%B0%A9%EB%B2%95%200-Windows%EB%B9%A0%EB%A5%B8%EC%84%A4%EC%B9%98%20_%20%EB%84%A4%EC%9D%B4%EB%B2%84%20%EC%B9%B4%ED%8E%98.pdf)
 
 - 섹션3-13강. [무게감 있게 설치하는 방법 1-1788853.pdf](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/%EB%AC%B4%EA%B2%8C%EA%B0%90%20%EC%9E%88%EA%B2%8C%20%EC%84%A4%EC%B9%98%ED%95%98%EB%8A%94%20%EB%B0%A9%EB%B2%95%201-1788853.pdf)
 
 - 섹션3-14강. [무게감 있게 설치하는 방법 2-1788853.pdf](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/%EB%AC%B4%EA%B2%8C%EA%B0%90%20%EC%9E%88%EA%B2%8C%20%EC%84%A4%EC%B9%98%ED%95%98%EB%8A%94%20%EB%B0%A9%EB%B2%95%202-1788853.pdf)
 
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

## 섹션1-5강. 컨테이너 한방정리
 - [1-1-1 컨테이너 한방정리2 - 인프런.pdf](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/1-1-1%20%EC%BB%A8%ED%85%8C%EC%9D%B4%EB%84%88%20%ED%95%9C%EB%B0%A9%EC%A0%95%EB%A6%AC2%20-%20%EC%9D%B8%ED%94%84%EB%9F%B0.pdf)


## 섹션1-7강. 쿠버네티스 흐름으로 이해하는 컨테이너
 - [쿠버네티스 흐름으로 이해하는 컨테이너](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/%EC%BF%A0%EB%B2%84%EB%84%A4%ED%8B%B0%EC%8A%A4%20%ED%9D%90%EB%A6%84%EC%9C%BC%EB%A1%9C%20%EC%9D%B4%ED%95%B4%ED%95%98%EB%8A%94%20%EC%BB%A8%ED%85%8C%EC%9D%B4%EB%84%88%20(%EC%9D%BC%ED%94%84%EB%A1%9C%20%EC%B6%94%EA%B0%80%EC%A0%95%EB%A6%AC%20%EB%B2%84%EC%A0%843).pdf)
 
## 섹션4-18강. 실무에서 느껴본 쿠버네티스가 정말 편한 이유
 - [실무에서 느껴본 쿠버네티스가 정말 편한 이유](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/1-1-3%20%EC%8B%A4%EB%AC%B4%EC%97%90%EC%84%9C%20%EB%8A%90%EA%BB%B4%EB%B3%B8%20%EC%BF%A0%EB%B2%84%EB%84%A4%ED%8B%B0%EC%8A%A4%EA%B0%80%20%EC%A0%95%EB%A7%90%20%ED%8E%B8%ED%95%9C%20%EC%9D%B4%EC%9C%A0%20-%20%EC%9D%B8%ED%94%84%EB%9F%B0-1788853.pdf)


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
 - [yaml : 쿠버네티스가 정말 편한 이유[체험 App배포](쿠버네티스 대표 기능).md](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/%EC%BF%A0%EB%B2%84%EB%84%A4%ED%8B%B0%EC%8A%A4%EA%B0%80_%EC%A0%95%EB%A7%90_%ED%8E%B8%ED%95%9C_%EC%9D%B4%EC%9C%A0_%EC%B2%B4%ED%97%98App%EB%B0%B0%ED%8F%AC.md
 
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
   ```yaml
    spec:
         containers:
            - name: app-1-2-2-1
              image: 1pro/app-update  # 수정
    ```
   - kubectl 명령으로 할 경우
     - kubectl set image -n default deployment/app-1-2-2-1 app-1-2-2-1=1pro/app-update
 - 기동되지 않는 App 업데이트 (RollingUpdate 테스트)     
   - Namespace: default &gt; 디플로이먼트 &gt; ... &gt; 편집
   ```yaml
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

## 섹션7-26강. Object 그려보며 이해하기 1/2 (💻 실습포함)
 - 실습 자료실 : https://cafe.naver.com/kubeops/36
 - Namespace, Deployment, Service, Configmap/Secret, PVC/PV, HPA 추가
 - [Object 그려보며 이해하기 1_2.md](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/Object%20%EA%B7%B8%EB%A0%A4%EB%B3%B4%EB%A9%B0%20%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0%201_2.md)
 
### Namespace
오브젝트들을 그룹핑 해주는 역할
 - name
 - labels
 - 삭제 시 하위 모든 오브젝트 삭제.
 - PV는 Cluster 레벨이므로 별도 삭제
  
### Deployment
Pod를 만들고 업그레이드 해주는 역할
 - namespace : 그룹핑 될 Namespace 명 설정
 - name : 한 오브젝트 에서 중복 불가
 - lables
 - selector
 - replicas : Pod 개수 설정
 - strategy
   - type : RollingUpdate
 - template : Pod 명세
   - spec
     - nodeSelector
       - kubernetes.io/hostname :k8s-master
   - containers
     - name : 컨테이너명
     - image : 컨테이너 이미지명(docker hub에서 다운받을 이름)
     - envForm
       - configMapRef
         - name : app의 환경변수 (ConfigMap 이름과 동일하게 설정) 
     - startupProbe : app이 잘 기동 되었는지 확인
     - readinessProbe : app에 Traffic을 연결 할 것인지 확인(서비스를 할 것인지)
     - livenessProbe : app이 정상이 아니면 재시작 할 것인지 확인
     - resource : 자원 할당
     - volumeMounts(여러개 설정 가능)
       - name : files (volumes name node 값)
       - mountPath : /usr/src/myapp/dev/files ==> 물리적 경로
       - name : secret-datasource (volumes name node 값)
       - mountPath : /usr/src/myapp/datasource ==> 물리적 경로       

### Service
Pod에 Traffic을 연결해 주는 역할
 - Pod에는 서비스를 여러개 붙일 수 있음
 

### ConfigMap
Pod에 환경변수를 설정 해주는 역할

### Secret
Pod에 보안이 필요한 설정 해주는 역할
 - stringData 에 있는 내용을 Pod 안에 파일로 만듬

### PVC
PV(Cluster 레벨) 설정에서 해당 Namespace가 사용할 저장 공간 설정

### PV
Cluster 레벨에서 저장 공간 설정

### HPA
부하에 따라 Pod를 늘리거나 줄이는 역할
 - Scale대상 : Deployment
 - minReplicas / maxReplicas 개수 설정에서
 - cpu 사용율 등 늘리는 조건 설정
 - 다음 replica 를 늘릴때의 Term 설정(600초)
 - 이벤트 등 상황에 따른 HPA를 여러개 만들수 있음
  
### 강의에서 배포한 Object 삭제
 - kubectl delete ns anotherclass-123
 - kubectl delete pv api-tester-1231-files

## 섹션7-27강. Object 그려보며 이해하기 2/2 (💻 실습포함)

### Prometheus labels node 내용 설명
```yaml
labels:
   part-of : kube-prometheus
   component : prometheus
   name : prometheus
   instance : k8s
   version :  2.33.0
```
```yaml
labels:
   part-of : kube-prometheus
   component : expoter
   name : kube-state-metrics ==> kube 성능
   instance : k8s
   version :  xxx
```
```yaml
labels:
   part-of : kube-prometheus
   component : expoter
   name : node-exporter ==> vm 성능
   instance : k8s
   version :  xxx
```
```yaml
labels:
   part-of : kube-prometheus
   component : grafana
   name : grafana
   instance : k8s
   version :  2.33.0
```
 - part-of : App 구성 전체 이름
 - component : 구성요소(prometheus, exporter, grafana)
 - name : App 개별 이름
 - instance : prometheus를 목적에 따라 여러개 설치 할 경우의 식별할 이름(일반적으로 : name + 인스턴스이름)
 - version : App 버전

### Object Naming 룰 예시
 - Namespace : monitoring
 - StatefulSet : prometheus-k8s
 - Service : prometheus-k8s
 - ConfigMap : prometheus-k8s-rule


### ConfigMap
 - 여러개 만들수 있음
 - 외부에서 App에 전달하는 모든 데이터들을 configmap에 담을 수 있음
 - prometheus 의 configmap에는 성능 관련 계산 공식이 있음(기동시 초기 데이터로 사용)

### Managed-by
 - 쿠버네티스의 권고 label 정보
 - 어떤 도구로 배포 됐는지 설정
   - dashboard : "Object 그려보며 이해하기" yaml 정보들을 대시보드를 통해 등록 함


### 강의에서의 오브젝트 구성요소
 - Namespace : anotherclass-123
 - Deployment : api-tester-1231
    ```yaml
    spec:
      strategy : RollingUpdate
      replicas : 2
    ```

    - 위 설정을 기반으로 ReplicaSet 생성
    - 이름 : api-tester-1231-xxx(임의의 문자 자동 부여) ==> ReplicaSet 이름
      - ReplicaSet을 기반으로 Pod 생성
      - 이름 : api-tester-1231-xxx-yyy(임의의 문자 자동 부여) ==> Pod 이름
        - Pod의 lables(spec.metadata.labels)
            ```yaml
            labels:
              part-of: k8s-anotherclass
              component: backend-server
              name: api-tester
              instance: api-tester-1231
              version: 1.0.0
            ```
            - App 정보를 파악하기 위한 용도
            - selector와 연결해서 두 오브젝트를 연결하는 용도
        - ReplicaSet의 selector(spec.selector.matchLabels) : Pod와 연결
            ```yaml
            matchLabels:
              part-of: k8s-anotherclass
              component: backend-server
              name: api-tester
              instance: api-tester-1231
            ```
          - ReplicaSet의 selector의 내용은 모두 Pod의 lables에 포함되어야 함
            - Pod의 lables 에 추가로 더있는 정보는 가능
            - 반대는 불가
            - instance은 필수 이며 나머지는 선택 사항
    - selector와 labels의 연결
        ```
        Deployment(selector) ─ ReplicaSet(labels) => 참고)공백특수문자 : '　'
        ······················ ReplicaSet(selector)· ─ Pod(labels)
        ······················ Service(selector)···· ─ Pod(labels)
        PVC(selector) ─ PV(labels)
        ```
### 쿠버네티스의 Object간 연결하는 방법

 - 방법1) labels <-> selector
    ```
    Deployment(selector) ─ ReplicaSet(labels) => 참고)공백특수문자 : '　'
    ······················ ReplicaSet(selector)· ─ Pod(labels)
    ······················ Service(selector)···· ─ Pod(labels)
    PersistentVolumeClaim(selector) ─ PersistentVolume(labels)
    ```
 - 방법2) object 내에서 대상을 연결하는 속성
    ```
    HPA(scaleTargetRef.name 속성) ─ Deployment(labels.instance 속성)
    Pod(configMapRef.name 속성) ─ ConfigMap(metadata.name 속성)
    Pod(persistentVolumeClaim.claimName 속성) ─ PersistentVolumeClaim(metadata.name 속성 or matchLabels.instance)
    Pod(secret.secretName 속성) ─ Secret(metadata.name 속성)
    ```
### 쿠버네티스가 만든 Master Node 설정
    ```
    Pod(nodeSelector.kubernetes.io/hostname) : k8s-master
    PersistentVolume(nodeAffinity.required.nodeSelectorTerms.matchExpressions) : - {key: kubernetes.io/hostname, operator: In, values: [k8s-master]}
    ```

### Selector
 - Service
    ```yaml
    selector:
      part-of: k8s-anotherclass
      component: backend-server
      name: api-tester
      instance: api-tester-1231
    ```
  - PersistentVolumeClaim
    ```yaml
    matchLabels:
      part-of: k8s-anotherclass
      component: backend-server
      name: api-tester
      instance: api-tester-1231-files
    ```   
### 강의자료
 - [쿠버네티스 첫 오브젝트 잘 끼우기 - object 그려보며 이해하기](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/1-2-1%20%EC%BF%A0%EB%B2%84%EB%84%A4%ED%8B%B0%EC%8A%A4%20%EC%B2%AB%20%EC%98%A4%EB%B8%8C%EC%A0%9D%ED%8A%B8%20%EC%9E%98%20%EB%81%BC%EC%9A%B0%EA%B8%B0%20-%20object%20%EA%B7%B8%EB%A0%A4%EB%B3%B4%EB%A9%B0%20%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0%20-%20%EC%9D%B8%ED%94%84%EB%9F%B0-1788853.pdf)


## 섹션8-29강. Application 기능을 이해하기 - Pod (probe) 자료
 - [쿠버네티스 첫 오브젝트 잘 끼우기 - application 기능으로 이해하기(1) - Pod(probe)](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/1-2-2%20%EC%BF%A0%EB%B2%84%EB%84%A4%ED%8B%B0%EC%8A%A4%20%EC%B2%AB%20%EC%98%A4%EB%B8%8C%EC%A0%9D%ED%8A%B8%20%EC%9E%98%20%EB%81%BC%EC%9A%B0%EA%B8%B0%20-%20application%20%EA%B8%B0%EB%8A%A5%EC%9C%BC%EB%A1%9C%20%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0(1)%20-%20Pod(probe).pdf)


## 섹션8-29강. Probe 자료

 - [쿠버네티스 첫 오브젝트 잘 끼우기 - application 기능으로 이해하기(1) - Pod(probe)](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/1-2-2%20%EC%BF%A0%EB%B2%84%EB%84%A4%ED%8B%B0%EC%8A%A4%20%EC%B2%AB%20%EC%98%A4%EB%B8%8C%EC%A0%9D%ED%8A%B8%20%EC%9E%98%20%EB%81%BC%EC%9A%B0%EA%B8%B0%20-%20application%20%EA%B8%B0%EB%8A%A5%EC%9C%BC%EB%A1%9C%20%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0(1)%20-%20Pod(probe).pdf)

 - startupProbe
   - 설정된 간격으로 호출을 하고 한번이라도 성공하면 성공으로 간주하고 readinessProbe, livenessProbe 를 호출
 - readinessProbe
   - 성공하면 외부서비스를 Pod가 받을 수 있는 상태로 변경
 - livenessProbe
   - App가 살아있는지 확인을 하고 설정한 회수 만큼 실패하면 App을 재기동
   
## 섹션8-31강. Application 로그를 통한 프로브 동작 분석 (💻 실습포함)
 - https://cafe.naver.com/kubeops/39
 - [Application 기능으로 이해하기-Probe(Application 로그를 통한 프로브 동작 분석/Application 동작 중심의 프로브 이해)](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/Application%20%EA%B8%B0%EB%8A%A5%EC%9C%BC%EB%A1%9C%20%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0-Probe(Application%20%EB%A1%9C%EA%B7%B8%EB%A5%BC%20%ED%86%B5%ED%95%9C%20%ED%94%84%EB%A1%9C%EB%B8%8C%20%EB%8F%99%EC%9E%91%20%EB%B6%84%EC%84%9D_Application%20%EB%8F%99%EC%9E%91%20%EC%A4%91%EC%8B%AC%EC%9D%98%20%ED%94%84%EB%A1%9C%EB%B8%8C%20%EC%9D%B4%ED%95%B4)%20_%20%EB%84%A4%EC%9D%B4%EB%B2%84%20%EC%B9%B4%ED%8E%98.pdf)

## 섹션8-32강. Application 동작 중심의 프로브 이해
 - https://cafe.naver.com/kubeops/39
 - [Application 기능으로 이해하기-Probe(Application 로그를 통한 프로브 동작 분석/Application 동작 중심의 프로브 이해)]()














다양한 인터페이스로 타 시스템 요청/응답 연계
 - RESTful API, WSDL 2.0 등
 
다양한 데이터 형식으로 타 시스템 요청/응답 연계
 - 데이터 형식: XML 1.0, JSON, Fixed Langth, Delimeter 등

UMS 등 DB를 통한 연계

Elastic Search 연계

DX UIM, OnTune 을 통한 장애감지 및 시스템 리소스 모니터링

Redis를 통한 세션정보 공유
 - ESXi Host에 각각 Redis용 VM을 생성하여 고가용성으로 구성 






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