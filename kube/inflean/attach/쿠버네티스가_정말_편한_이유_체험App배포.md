## [섹션5] 쿠버네티스가 정말 편한 이유[체험 App배포](쿠버네티스 대표 기능)
 - https://cafe.naver.com/kubeops/31
 
### 적용 
 - dashboard 접속 > Namespace [default] > [+] 버튼 > [입력을 통해 생성] > yaml 내용 붙여넣기 > 업로드

### yaml 내용
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