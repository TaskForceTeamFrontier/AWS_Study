# aws_process

ReactJS SprintBoot3 MySQL

## Ref

- Search Result
    - [Google / AWS EC2](https://www.google.com/search?q=aws+ec2)
    - [Google / AWS React SpringBoot MySQL](https://www.google.com/search?q=aws+react+springboot+mysql)

- Each Doc
    - [EC2 설정](https://olrlobt.tistory.com/83)
    - [[AWS] 프리티어 종료(EC2, Elastic IP, RDS, Route 53 등 종료하기)](https://dev-jwblog.tistory.com/91)

## 프리티어 EC2 설정

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
- 스토리지 구성
    - 프리티어 / 30GiB gp3 루트 볼륨륨
- 인스턴스 시작 선택

## MySQL

- 검색창 RDS 검색
- RDS 선택
- 데이터베이스 생성 선택
- MySQL 선택
- MySQL 버전선택
- 템플릿 > 프리티어 선택
- DB 인스턴스 식별자 입력
- 마스터 사용자 이름 설정
- 비밀번호 설정
- 

## ReactJS 

## SprintBoot3 
