# mysql-opentutorials

## 설치 및 실행 방법

설치 : https://bitnami.com/stack/wamp

실행 : 위의 링크에서 파일 설치 후, 설치 경로에서 '\mysql\bin'로 이동(명령어 프롬프트 활용)
```
mysql -uroot -p //비밀번호 입력하고 데이터베이스 서버에 접속하기
```

## 데이터베이스 명령어
```
CREATE DATABASE 데이터베이스이름;     //데이터베이스 생성
DROP DATABASE 데이터베이스이름;       //데이터베이스 삭제
SHOW DATABASES;                     //데이터베이스 목록 보기
USE 데이터베이스이름;                 //해당 데이터베이스를 사용함
```

## 테이블 명령어
```
CREATE TABLE 테이블이름(             //테이블 생성
  ...
)
```
