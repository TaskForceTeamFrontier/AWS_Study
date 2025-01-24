# aws_process

ReactJS SprintBoot3 MySQL

## Ref

- Search Result
    - [Google / AWS EC2](https://www.google.com/search?q=aws+ec2)
    - [Google / AWS React SpringBoot MySQL](https://www.google.com/search?q=aws+react+springboot+mysql)

- Each Doc
    - [EC2 설정](https://olrlobt.tistory.com/83)
    - [[AWS] 프리티어 종료(EC2, Elastic IP, RDS, Route 53 등 종료하기)](https://dev-jwblog.tistory.com/91)

## AWS 과금 방지지

## AWS 프리티어 EC2 설정

- AWS Region 설정 : 아시아 태평양 ( 서울 )
- 콘솔 홈 > 모든 서비스 보기
- 컴퓨팅 > EC2 선택
- 인스턴스 시작 선택
- 이름 및 태그 설정 : test-webapp
- OS Image 선택
    - Ubuntu 
    - Ubuntu Server 24.04 LTM
- 인스턴스 유형
    - t2.micro / 프리티어 사용 가능
- 키페어 ( 로그인 )
    - RSA / .pem 선택
    - 키페어 생성
- 네트워크 설정
    - 방화벽 / 보안 그룹 생성
    - 다음에서 SSH 트래픽 허용
    - 인터넷에서 HTTPS 트래픽 허용
    - 인터넷에서 HTTP 트래픽 허용
- 스토리지 구성
    - 프리티어 / 30GiB gp3 루트 볼륨륨
- 인스턴스 시작 선택

## RDS / MySQL

- AWS Region 설정 : 아시아 태평양 ( 서울 )
- 콘솔 홈 > 모든 서비스 보기
- 데이터베이스 > RDS 선택
- 데이터베이스 생성 선택
- 데이터베이스 생성 방식 > 표준 생성
- 엔진 옵션 > MySQL
- 템플릿 > 프리 티어 선택
- 설정
    - DB 인스턴스 식별자 > 이름 설정
    - 마스터 사용자 이름 작성
    - 자격 증명 관리 > 자체 관리 선택
    - 마스터 암호 설정
- 스토리지
    - 스토리지 유형 > gp3
    - 할당 스토리지 > 20 GiB 
- 연결
    - 컴퓨팅 리소스 > EC2 컴퓨팅 리소스에 연결 안 함.
    - 퍼블릭 액세스 > 예
    - 자동 백업 > 제거
- 추가구성
    - 초기 데이터베이스 이름 > 이름 설정
    - 기본값 그대로 구성
- 데이터베이스 생성 선택

## RDS / VPC 보안 그룹

- 생성된 DB 식별자 선택
- VPC 보안 그룹 설정
- 보안 그룹 ID 선택
- 인바운드 규칙 편집 선택
- 규칙 추가
    - 사용자 지정 IP / 3306 / Anywhere IPv4 / 설명 외부 접속
    - 사용자 지정 IP / 3306 / Anywhere IPv6 / 설명 외부 접속
    - 사용자 지정 IP / 3306 / 내 IP / 설명 외부 접속
- 규칙 저장

## RDS / 외부접속 / 안될 경우
- 콘솔 홈 > 모든 서비스 > 네트워킹 및 콘텐츠 전송 > VPC 선택
- 라우팅 테이블 선택 / RDS 연결된 것.
- 라우팅 편집
- 라우팅 추가
- 0.0.0.0/0 선택 / 인터넷게이트웨이 선택 / igw-자동선택
- 변경 사항 저장

## ReactJS 

## SprintBoot3 
