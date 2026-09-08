## 섹션4-12강.

#### 설치 주소
 - Windows: https://cafe.naver.com/kubeops/21
 - Mac : https://cafe.naver.com/kubeops/91
 
 
#### 접속 정보
 - 192.168.56.30
 - root / vagrant

#### Pod 확인
 - k get pods -A
 - Dashboard-Metrics Pending 상태 지속 문제 해결
   - kubectl taint nodes  k8s-master node-role.kubernetes.io/control-plane- 
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