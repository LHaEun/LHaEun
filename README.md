# 2020년 1학기, 빅데이터 캡스톤
# IoT 디바이스를 위한 보안 프로토콜 개발(공개 레파지토리에 배포되는 악성코드를 자동화 탐지)
팀명: IDSs_a
팀원: 이하은
지도교수: 조효진 교수님
참여기업: 현대오토에버 이정호 연구원

#프로젝트 개요
많은 개발자들은 Git Hub를 통해 소스코드를 공유한다. 하지만 소수의 사람들이 소스코드 속에 멀웨어를 숨겨두어 사용자들에게 피해를 입힌다.


#기대효과 및 활용방안
소스코드에 숨어있는 멀웨어를 탐지하여 사용자가 이를 피해갈 수 있게 하여 안전한 Git Hub 사용으로 이어질 수 있다.

# 개발 과정
악성코드 자동화 탐지툴을 만들기 위해서 사용자로부터 받은 파일의 로그를 읽고 저장하고 보기 위해 VM server에 ELK를 설치하고 서로 연동했다. 
logstash를 이용해 로그를 가져와서 Elasticsearch로 데이터를 보낸 후 Elasticsearch안에 구현한 DB에 저장 후 YARA rule로 검색한다. 이때 Kibana를 이용해 
로그를 확인한다. 

1. ELK를 설치하기 전 JAVA 설치
<img width="331" alt="캡처" src="https://user-images.githubusercontent.com/59590254/80512820-0d1a3d80-89b9-11ea-9954-b580a09ae94f.PNG">

2.ELK 설치 및 연동
1)logstash: 각종 로그를 가져와서 JSON 형태로 만들어 Elasticsearch로 데이터를 전송한다.
<img width="642" alt="캡처" src="https://user-images.githubusercontent.com/59590254/80514086-fbd23080-89ba-11ea-91d0-aa89e3722415.PNG">

2)Elasticsearch: 검색 및 분석 엔진, DB 저장


3)Kibana: Elasticsearch에 저장된 데이터를 사용자에게 Dashboard 형태로 보여주는 시각화 솔루션
<img width="186" alt="캡처" src="https://user-images.githubusercontent.com/59590254/80513842-a0a03e00-89ba-11ea-98c0-a4f34dfc9a30.PNG">



