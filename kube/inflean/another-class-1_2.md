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
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=205408&subtitleLanguage=ko

**자료:**[실무에서 느껴본 쿠버네티스가 정말 편한 이유](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/1-1-3%20%EC%8B%A4%EB%AC%B4%EC%97%90%EC%84%9C%20%EB%8A%90%EA%BB%B4%EB%B3%B8%20%EC%BF%A0%EB%B2%84%EB%84%A4%ED%8B%B0%EC%8A%A4%EA%B0%80%20%EC%A0%95%EB%A7%90%20%ED%8E%B8%ED%95%9C%20%EC%9D%B4%EC%9C%A0%20-%20%EC%9D%B8%ED%94%84%EB%9F%B0-1788853.pdf)

 - [쿠버네티스 흐름으로 이해하는 컨테이너](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/%EC%BF%A0%EB%B2%84%EB%84%A4%ED%8B%B0%EC%8A%A4%20%ED%9D%90%EB%A6%84%EC%9C%BC%EB%A1%9C%20%EC%9D%B4%ED%95%B4%ED%95%98%EB%8A%94%20%EC%BB%A8%ED%85%8C%EC%9D%B4%EB%84%88%20(%EC%9D%BC%ED%94%84%EB%A1%9C%20%EC%B6%94%EA%B0%80%EC%A0%95%EB%A6%AC%20%EB%B2%84%EC%A0%843).pdf)
 
## 섹션4-18강. 실무에서 느껴본 쿠버네티스가 정말 편한 이유
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=205408&subtitleLanguage=ko

**자료:**[실무에서 느껴본 쿠버네티스가 정말 편한 이유](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/1-1-3%20%EC%8B%A4%EB%AC%B4%EC%97%90%EC%84%9C%20%EB%8A%90%EA%BB%B4%EB%B3%B8%20%EC%BF%A0%EB%B2%84%EB%84%A4%ED%8B%B0%EC%8A%A4%EA%B0%80%20%EC%A0%95%EB%A7%90%20%ED%8E%B8%ED%95%9C%20%EC%9D%B4%EC%9C%A0%20-%20%EC%9D%B8%ED%94%84%EB%9F%B0-1788853.pdf)

## 섹션4-19강. 쿠버네티스 표준 생태계로 편해진 IT 인프라 구축
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=205421&subtitleLanguage=ko


## 섹션5-20강. 모니터링 설치 - Loki-Stack (💻 실습포함)
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=205425&subtitleLanguage=ko

**자료:** https://cafe.naver.com/kubeops/30

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
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=162844&subtitleLanguage=ko

**자료:**https://cafe.naver.com/kubeops/36
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
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=205447&subtitleLanguage=ko

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
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=205452&subtitleLanguage=ko
**자료:**https://cafe.naver.com/kubeops/39

**자료:**[Application 기능으로 이해하기-Probe(Application 로그를 통한 프로브 동작 분석_Application 동작 중심의 프로브 이해) _ 네이버 카페.pdf](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/Application%20%EA%B8%B0%EB%8A%A5%EC%9C%BC%EB%A1%9C%20%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0-Probe(Application%20%EB%A1%9C%EA%B7%B8%EB%A5%BC%20%ED%86%B5%ED%95%9C%20%ED%94%84%EB%A1%9C%EB%B8%8C%20%EB%8F%99%EC%9E%91%20%EB%B6%84%EC%84%9D_Application%20%EB%8F%99%EC%9E%91%20%EC%A4%91%EC%8B%AC%EC%9D%98%20%ED%94%84%EB%A1%9C%EB%B8%8C%20%EC%9D%B4%ED%95%B4)%20_%20%EB%84%A4%EC%9D%B4%EB%B2%84%20%EC%B9%B4%ED%8E%98.pdf)

 - [쿠버네티스 첫 오브젝트 잘 끼우기 - application 기능으로 이해하기(1) - Pod(probe)](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/1-2-2%20%EC%BF%A0%EB%B2%84%EB%84%A4%ED%8B%B0%EC%8A%A4%20%EC%B2%AB%20%EC%98%A4%EB%B8%8C%EC%A0%9D%ED%8A%B8%20%EC%9E%98%20%EB%81%BC%EC%9A%B0%EA%B8%B0%20-%20application%20%EA%B8%B0%EB%8A%A5%EC%9C%BC%EB%A1%9C%20%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0(1)%20-%20Pod(probe).pdf)

 - startupProbe
   - 설정된 간격으로 호출을 하고 한번이라도 성공하면 성공으로 간주하고 readinessProbe, livenessProbe 를 호출
 - readinessProbe
   - 성공하면 외부서비스를 Pod가 받을 수 있는 상태로 변경
 - livenessProbe
   - App가 살아있는지 확인을 하고 설정한 회수 만큼 실패하면 App을 재기동
   
## 섹션8-31강. Application 로그를 통한 프로브 동작 분석 (💻 실습포함)
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=205452&subtitleLanguage=ko
**자료:**https://cafe.naver.com/kubeops/39

**자료:**[Application 기능으로 이해하기-Probe(Application 로그를 통한 프로브 동작 분석_Application 동작 중심의 프로브 이해) _ 네이버 카페.pdf](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/Application%20%EA%B8%B0%EB%8A%A5%EC%9C%BC%EB%A1%9C%20%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0-Probe(Application%20%EB%A1%9C%EA%B7%B8%EB%A5%BC%20%ED%86%B5%ED%95%9C%20%ED%94%84%EB%A1%9C%EB%B8%8C%20%EB%8F%99%EC%9E%91%20%EB%B6%84%EC%84%9D_Application%20%EB%8F%99%EC%9E%91%20%EC%A4%91%EC%8B%AC%EC%9D%98%20%ED%94%84%EB%A1%9C%EB%B8%8C%20%EC%9D%B4%ED%95%B4)%20_%20%EB%84%A4%EC%9D%B4%EB%B2%84%20%EC%B9%B4%ED%8E%98.pdf)

## 섹션8-32강. Application 동작 중심의 프로브 이해
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=205449&subtitleLanguage=ko

**자료:**https://cafe.naver.com/kubeops/39

## 섹션8-33강. Application 동작 중심의 프로브 이해 (💻 실습)
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=205450&subtitleLanguage=ko

**자료:**https://cafe.naver.com/kubeops/39

  - [App 초기화] 중 시스템 연동 작업을 하고, [User 초기화] 중에 초기 데이터 로딩 작업이 있음. 그리고 이 작업이 다 끝나야 [기동완료] 가 되는 App 기동 상황

  - startupProbe가 5초 간격으로 호출 되고, 성공할 때까지 반복, 성공 후 readinessProbe와 livenessProbe가 시작

  - livenessProbe는 바로 성공을 하지만, readinessProbe는 처음 실패 후에 [기동완료] 가 되서야 성공을 함

  - livenessProbe와 readinessProbe는 10초 간격으로 계속 호출 됨

    ```
    ﻿// 1번 API - 외부 API 실패
    curl http://192.168.56.30:31231/hello

    ﻿// 2번 API 
    // 외부 API 실패
    curl http://192.168.56.30:31231/hello

    // 내부 API 성공
    kubectl exec -n anotherclass-123 -it api-tester-1231-7459cd7df-2hdhk -- curl localhost:8080/hello
    kubectl exec -n anotherclass-123 -it <my-pod-name> -- curl localhost:8080/hello

    ﻿// 3번 API - 외부 API 성공
    curl http://192.168.56.30:31231/hello

    ﻿// 4번 API
    // 트래픽 중단 - (App 내부 isAppReady를 False로 바꿈)
    curl http://192.168.56.30:31231/traffic-off
    // 외부 API 실패
    curl http://192.168.56.30:31231/hello﻿
    // 트래픽 재개 - (App 내부 isAppReady를 True로 바꿈)
    kubectl exec -n anotherclass-123 -it api-tester-1231-7459cd7df-2hdhk -- curl localhost:8080/traffic-on

    ﻿// 5번 API - 장애발생 (App 내부 isAppLive를 False로 바꿈)
    curl http://192.168.56.30:31231/server-error
    ```
- 응용과제
  - **응용1** : startupProbe가 실패 되도록 설정해서 Pod가 무한 재기동 상태가 되도록 설정해 보세요. (여러분들이 가장 많이 겪게될 Pod 에러입니다)
  
  - **응용2** : 일시적 장애 상황(App 내부 부하 증가)가 시작 된 후, 30초 뒤에 트래픽이 중단되고, 3분 뒤에는 App이 재기동 되도록 설정해 보세요.(아래 API를 날리면 readinessProbe와 livenessProbe가 동시에 실패하게 됩니다)

    ```
    // 부하 증가 - (App 내부 isAppReady와 isAppLive를 False로 바꿈)
    curl http://192.168.56.30:31231/server-load-on

    // 외부 API 실패
    curl http://192.168.56.30:31231/hello

    ﻿// 부하 감소 API - (App 내부 isAppReady와 isAppLive를 True로 바꿈)
    curl http://192.168.56.30:31231/server-load-off
    ​```
  - **응용3** : Secret 파일(/usr/src/myapp/datasource/postgresql-info.yaml)이 존재하는지 체크하는 readinessProbe를 만들어 보세요.(꼭 API를 날리는 것만이 readinessProbe 활용의 전부는 아닙니다)

- [Application 기능으로 이해하기-Probe(응용 과제)](https://cafe.naver.com/kubeops/40)

## 섹션8-37강. Configmap, Secret 기본 개념
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=174651&subtitleLanguage=ko

**자료:**https://cafe.naver.com/kubeops/43

**자료:**[1-2-3_쿠버네티스_첫_오브젝트_잘_끼우기_-_application_기능으로_이해하기(2)_-_Configmap,_Secret_-_인프런2.pdf](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/1-2-3_%EC%BF%A0%EB%B2%84%EB%84%A4%ED%8B%B0%EC%8A%A4_%EC%B2%AB_%EC%98%A4%EB%B8%8C%EC%A0%9D%ED%8A%B8_%EC%9E%98_%EB%81%BC%EC%9A%B0%EA%B8%B0_-_application_%EA%B8%B0%EB%8A%A5%EC%9C%BC%EB%A1%9C_%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0(2)_-_Configmap%2C_Secret_-_%EC%9D%B8%ED%94%84%EB%9F%B02.pdf)

## 섹션8-38강. Configmap, Secret 기본 개념
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=205460&subtitleLanguage=ko

**자료:**https://cafe.naver.com/kubeops/43

## 섹션9-43강. PV/PVC (local, hostPath)
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=174653&subtitleLanguage=ko

**자료:**https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/1-2-4%20%EC%BF%A0%EB%B2%84%EB%84%A4%ED%8B%B0%EC%8A%A4%20%EC%B2%AB%20%EC%98%A4%EB%B8%8C%EC%A0%9D%ED%8A%B8%20%EC%9E%98%20%EB%81%BC%EC%9A%B0%EA%B8%B0%20-%20application%20%EA%B8%B0%EB%8A%A5%EC%9C%BC%EB%A1%9C%20%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0(3)%20-%20PV_PVC%2C%20Deployment%2C%20Service%2C%20HPA%20-%20%EC%9D%B8%ED%94%84%EB%9F%B0-1788853.pdf

**자료:**https://cafe.naver.com/kubeops/49

## 섹션9-44강. Deployment (Recreate, RollingUpdate-maxUnavailable, maxSurge)
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=205470&subtitleLanguage=ko

**자료:**https://cafe.naver.com/kubeops/49

- Recreate(Replicas가 2로 설정 된 경우)
  - 기존 파드 모두 삭제.
  - 새 파드 두개 생성
 
- RollingUpdate(Replicas가 2로 설정 된 경우)
  - 순서
    - Pod1 삭제 Pod1-1 생성
    - Pod2 삭제 Pod1-2 생성
  - 업데이트 중 자원 사용률이 150% 증가
  - 신규 서비스(Pod1-1), 구 서비스(Pod2) 가 동시에 서비스 됨
    - RollingUpdate 옵션 -> maxUnavailable : 25% ==> 업데이트 동안 최대 몇 개의 pod를 서비스 상태로 유지할 지...(총 pod 중 25%를 서비스 못하게 함)
      - 0% 인 경우 업데이트 동안 모든 pod가 서비스 됨
    - RollingUpdate 옵션 -> maxSurge : 25% ==> 새 pod를 최대 몇 개까지 동시에 생성할 지..
      - 100% 인 경우 업데이트 동안 replica 수 만큼 한번에 생성
    - maxUnavailable : 0%, maxSurge : 100% 인 경우 아래 Blue/Green 에 가까운 동작.
      - 순서
        - Pod1-1 생성
        - Pod1 삭제
        - Pod2-1 생성
        - Pod2 삭제
    - maxUnavailable : 100%, maxSurge : 100% 인 경우 Recreate와 동일하게 동작.
 
- Blue/Green(Replicas가 2로 설정 된 경우)
  - 순서
    - Pod1-1 생성
    - Pod1-2 생성
    - Pod1, Pod2 삭제
  - 업데이트 중 자원 사용률이 200% 증가
  - 동시에 서비스 안됨
  - 별도 배포 솔루션에서 제공
  

## 섹션9-45강. Service - Discovery, Publising, Registry, Load Balancing,
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=205471&subtitleLanguage=ko

**자료:**https://cafe.naver.com/kubeops/49

- Service.spec.selector 
  - Pod의 labels로 서로 연결됨
- Service.spec.type : 연결 타입 설정
  - ClusterIP : 내부에서만 연결됨(내부용 서비스)
  - NodePort : MasterNode에 port가 생성되면서 외부에서 접근이 가능하게 함.
- Service.spec.ports : 포트 정보 설정
  - targetPort : 8080 ==> 외부 또는 내부 포트를 Container Image 패키징 시 설정한 port와 연결
  - port : 80 ==> 내부 포트(동일한 namespace의 다른 pod, 다른 namespace의 pod에서 호출 시 사용)
    - 다른 namespace의 pod에서 호출 : http://<Service.metadata.name>.<namespace.metadata.name>:port(80)
    - port(80) -> targetPort(8080) -> pod(Container Image 생성시 port) 로 연결
  - nodePort : 18080 ==> 외부 포트(MasterNode에 자동 설정)
    - nodePort -> targetPort(8080) -> pod(Container Image 생성시 port) 로 연결
- Service.metadata.name 이 DNS로 등록되므로 http://<Service.metadata.name>:<Service.spec.ports.port>로 서비스 호출 가능
  - 서비스 디스커버리 기능
  - Service와 Pod는 생성될때 개별 IP가 부여됨
    - Pod삭제시 재생성시 신규 IP 부여됨.
  - IP가 바뀔 가능성이 있으므로 서비스 디스커버리 기능이 중요
- Deployment.spec.template.spec.containers.ports 에 port 정보를 설정할 수 있으며 포트 이름(name)을 정의할 수 있음
  - name : http ==> Service.spec.ports.targetPort에 name 기입이 가능함.
    - port가 변경되는 경우 Pod 정보만 수정하면 되고 Service에서는 이름으로 찾아갈 수 있음
  - containerPort : 8080 ==> Container Image 생성시 port 정보
    - 일반적인 경우 역할을 하지않는 정보성 속성이 지만 위 name 속성이 Service.spec.ports.targetPort에 사용된다면 연결 포트로서 동작.
- Pod(Deployment)가 Service에 등록되는 구조로 Pod가 삭제/생성시 IP가 변경되더라도 IP를 신경 쓸 필요가 없음
  - 서비스 레지스트리 기능
  
- Traffic 발생시(서비스요청시) Service에서 먼저 받아서 Pod로 분배하는 로드밸런싱 기능이 있음


## 섹션9-46강. HPA - Auto Scaling(아주 중요한 강의임)
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=205472&subtitleLanguage=ko

**자료:**https://cafe.naver.com/kubeops/49

- HPA.metadata.spec.scaleTargetRef : Deployment 를 지정하는 내용
- HPA.metadata.spec.minReplicas: 2, maxReplicas: 4 :  범위내에서 Deployment의 replicas 를 지정(기본 pods수)
- HPA.metadata.spec.metrics.`resource`.target(cpu).averageUtilization : 60
  - Deployment의 resources 에서 지정한 requests(cpu)에서 60%를 넘기면 ScaleOut, pod 평균으로 계산
- HPA.metadata.spec.metrics.`behavior`.scaleUp.stabilizationWindowSeconds: 120
  - ScaleOut 조건이 약 2분 정도 지속되면 ScaleOut 수행
  - scaleDown 옵션도 확인 필요

## 섹션11-50강. 각 리소스별 동작 (Probe, Service, Secret, HPA)
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=205488&subtitleLanguage=ko

**자료:**[1-2-5 쿠버네티스 첫 오브젝트 잘 끼우기 - component 동작으로 이해하기 - 인프런-1788853.pdf](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/1-2-4%20%EC%BF%A0%EB%B2%84%EB%84%A4%ED%8B%B0%EC%8A%A4%20%EC%B2%AB%20%EC%98%A4%EB%B8%8C%EC%A0%9D%ED%8A%B8%20%EC%9E%98%20%EB%81%BC%EC%9A%B0%EA%B8%B0%20-%20application%20%EA%B8%B0%EB%8A%A5%EC%9C%BC%EB%A1%9C%20%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0(3)%20-%20PV_PVC%2C%20Deployment%2C%20Service%2C%20HPA%20-%20%EC%9D%B8%ED%94%84%EB%9F%B0-1788853.pdf)

- Pod가 생성되는 과정
  1. kubectl로 Deployment 생성 API 호출
  2. kube-apiserver pod(Control Plane) 가 etcd pod를 통해 etcd에 deploement 정보 저장
    - Deployment 가 조회 가능상태, Dashboard에 표시 됨
  3. kube-controller-manager pod가 kube-apiserver pod를 통해 etcd를 모니터링 하다가 Deployment가 조회되면 ReplicaSet을 생성하라는 명령을 kube-apiserver pod로 보냄
  4. kube-apiserver pod(Control Plane) 가 etcd pod를 통해 etcd에 ReplicaSet 정보 저장
    - ReplicaSet 가 조회 가능상태, Dashboard에 표시 됨
  5. kube-controller-manager pod가 kube-apiserver pod를 통해 etcd를 모니터링 하다가 ReplicaSet이 조회되면 pod를 생성하라는 명령을 kube-apiserver pod로 보냄
  6. kube-apiserver pod(Control Plane) 가 etcd pod를 통해 etcd에 pod 정보 저장
  7. cube-scheduler pod가 kube-apiserver pod를 통해 etcd의 pod 정보를 모니터링 하다가 pod 정보(대상 Node, nodeSelector, resources 등)를 정보를 저장
  8. 대상 Node의 kubelet 이 kube-apiserver pod를 통해 자신의 노드 정보가 있는 pod 정보를 확인하면 container runtime를 통해 container를 생성요청
  9. containerd가  container 생성

- Probe 동작

  10. Container가 생성되면서 Probe정보를 확인하고 kubelet이 probe API를 주기적으로 호출

- Service 동작

  11. kubelet 이 nodePort(외부접속포트)를 확인하고 kube-proxy pod에게 네트워크를 생성해달라고 요청
  12. kube-proxy pod는 iptables 에 매핑룰 설정
    - 18080 포트로 요청에 대해 특정 Service 이름으로 매핑
  13. 외부에서 18080으로 요청이 오면 iptables를 참고해서 calico(CNI)가 실제 container로 Traffic을 전달함
  
- Secret 동작 : 메모리에 로딩됨
  - 변경내용을 주기적으로 업데이트 (즉시 반영 안됨)

- HPA 동작
 - 기본적으로 container 의 자원사용량은 containerd 가 알고 있음
 - kubelet 이 cpu, memory를 10초에 한 번씩 조회하고 있음
 - HPA의 metrics 설정을 한다고 해서 pod에 부하 발생시 동작하지는 않음
   1. metrics-server Addon Pod를 설치
     - metrics-server 60초 단위로 사용량을 수집/저장
   2. kube-controller-manager pod가 HPA의 metrics 설정 정보와 metrics-server 수집된 정보를 15초 마다 비교해서 Scalling을 발생 시킴
 -  Scalling을 발생하기 까지 최대 85초 소요 됨

## 섹션11-51강. 주요 컴포넌트 로그, 설정파일, 상태 확인 명령어 모음(위 내용)
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=205493&subtitleLanguage=ko

**자료:**https://cafe.naver.com/kubeops/61

- 주요 컴포넌트 구성, pod/container 로그, 동작(기동)로그 확인
    ```
    ▶ Resource 확인

    kubectl api-resources
    ​

    ▶ Cluster 주요 컴포넌트 로그 확인

    // 주요 컴포넌트 로그 보기 (kube-system)
    kubectl get pods -n kube-system
    kubectl logs -n kube-system etcd-k8s-master
    kubectl logs -n kube-system kube-scheduler-k8s-master
    kubectl logs -n kube-system kube-apiserver-k8s-master
    ...
    ​

    ▶ Master Node 파일 위치

    // 쿠버네티스 인증서 위치
    cd /etc/kubernetes
    ls /root/.kube/config

    // Control Plane Component Pod 생성 yaml 파일 위치
    ls /etc/kubernetes/manifests

    // 전체 Pod 로그
    /var/log/pods/<namespace_<pod-name>_<uid>/<number>.log
    /var/log/containers/<pod-name>_<namespace>_<container-name>_<container-id>.log
    ​

    ▶ 트러블 슈팅

    // kubelet 상태 확인
    1) systemctl status kubelet       // systemctl (restart or start) kubelet
    2) journalctl -u kubelet | tail -10

    // 상태 확인 -> 상세 로그 확인 -> 10분 구글링 -> VM 재기동 -> Cluster 재설치 ->  답을 찾을 때 까지 구글링

    // containerd 상태 확인
    1) systemctl status containerd
    2) journalctl -u containerd | tail -10

    // 노드 상태 확인
    1) kubectl get nodes -o wide
    2) kubectl describe node k8s-master

    // Pod 상태 확인
    1) kubectl get pods -A -o wide
    // Event 확인 (기본값: 1h)
    2-1) kubectl get events -A
    2-2) kubectl events -n anotherclass-123 --types=Warning  (or Normal)
    // Log 확인
    3-1) kubectl logs -n anotherclass-123 <pod-name> --tail 10    // 10줄 만 조회하기
    3-2) kubectl logs -n anotherclass-123 <pod-name> -f           // 실시간으로 조회 걸어 놓기
    3-3) kubectl logs -n anotherclass-123 <pod-name> --since=1m   // 1분 이내에 생성된 로그만 보기
    ```

- iptables 확인
  - iptables -t nat -L KUBE-NODEPORTS -n  | column -t
  - calico 버전 업데이트 되면서 nodePort 정보는 kubectl get svc -A를 통해서만 확인 가능


## 섹션13-52강. 인트로(DevOps 전체구성도)
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=205344&subtitleLanguage=ko

**자료:**[2-1-1 데브옵스 한방정리 - 인프런-1788853.pdf](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/2-1-1%20%EB%8D%B0%EB%B8%8C%EC%98%B5%EC%8A%A4%20%ED%95%9C%EB%B0%A9%EC%A0%95%EB%A6%AC%20-%20%EC%9D%B8%ED%94%84%EB%9F%B0-1788853.pdf)

|개발 환경|CI/CD 환경|인프라 환경|
|:-----:|:----:|:-----:|
|1. 개발도구 github 커밋|2. jenkins 소스 다운로드(github)|7. containerd 실행(pod생성)|
||3. Gradle Build(maven download)||
||4. Docker 이미지 생성||
||5. Docker 저장소 저장||
||6. Jenkins 배포(kubectl)||


## 섹션14-59강. CI/CD 서버환경을 구성하기 [구축 1~8단계] (💻 실습포함)
**강의:** https://www.inflearn.com/courses/lecture?courseId=330869&tab=curriculum&type=LECTURE&unitId=191169&subtitleLanguage=ko

**자료:**[2-1-2 손쉽게 데브옵스 환경을 구축하는 방법 - 인프런-1788853](https://github.com/omar-kang/doc/blob/main/kube/inflean/attach/2-1-2%20%EC%86%90%EC%89%BD%EA%B2%8C%20%EB%8D%B0%EB%B8%8C%EC%98%B5%EC%8A%A4%20%ED%99%98%EA%B2%BD%EC%9D%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EB%8A%94%20%EB%B0%A9%EB%B2%95%20-%20%EC%9D%B8%ED%94%84%EB%9F%B0-1788853.pdf

**자료:**https://cafe.naver.com/kubeops/84