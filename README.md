# inno3t-MSA-A1Begining
MSA시작하기-SpringCloud

## 1. Outer Arch
1. Spring Cloud을 기본으로 시작 (다음 버전에서 Istio와 통합)
2. 참조 문서
   - [교제- 스프링으로하는 마이크로서비스 구축](http://www.acornpub.co.kr/book/microservices-spring)
   - [전자 정부 "표준프레임워크 MSA 적용 개발 가이드" 참조](https://www.egovframe.go.kr/home/ntt/nttRead.do?menuNo=76&bbsId=171&nttId=1809)
   - [인프런 강의-Spring Cloud로 개발하는 마이크로서비스 애플리케이션(MSA)](https://www.inflearn.com/course/%EC%8A%A4%ED%94%84%EB%A7%81-%ED%81%B4%EB%9D%BC%EC%9A%B0%EB%93%9C-%EB%A7%88%EC%9D%B4%ED%81%AC%EB%A1%9C%EC%84%9C%EB%B9%84%EC%8A%A4/dashboard)
3. 1단계 목표 (~ 3/10)
   - 기본 Smaple Windows 10에서 수행가능한 환경 구성
   - 동일 버전을 Docker 버전으로 변경(Docker 서비스는 팀 개발장비(inno3t2)에 기동예정
     - 업무 서비스 컴포넌트는 Local에서도 수행 가능하도록 설정
   - 동일 버전을 K8s에서 기동(팀 개발 서버에 k8s 설치)
4. 2단계 목표 (~ 3/24)
   - DevOps 적용 (Git, Docker 이미지 생성, 로컬배포, Docker 배포, K8S 배포)      

## 2. Inner Arch 관련
1. 금융 기본 Sample 개발
   -표준 MSA (AP, DB 물리적 분리)
2. 동기 관련
   - 정합성을 위한 2PC 기능 
   - 보상거래(SAGA) 기능 구현
3. 비동기 
   - 이벤트 발생 유형별 개발: 순서 보장, 최종기준, Key값만 전송
   - kafka 이벤트
   - kafka Connector(DB2 DB,  File to DB)
   - Message 트랜잭션 관리 방안
4. 모델링 원칙 수립
   - 배치로 데이터 정합성 확인 방안
   - 일괄 재처리 방안
   - 원장 version 관리
5. 배치 처리 방안
   - 고객, 원장이 물리적 분리 상태에서 전체 고객의 잔액을 일괄 생성하는 방법(File)- Join이 불가능한 상태
   



