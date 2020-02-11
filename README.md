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
  id INT(11) NOT NULL AUTO_INCREMENT,     // id 라는 이름의 컬럼을 INT형으로 생성. NULL값을 허용하지 않고 자동 증가하는 설정
  title VARCHAR(100) NOT NULL,
  description TEXT NULL,
  created DATETIME NOT NULL,
  author VARCHAR(30) NULL,
  profile VARCHAR(100) NULL,
  PRIMARY KEY(id)
);
```

##SQL Insert 구문 (데이터 행 추가하기)
```
INSERT INTO 테이블이름 (타입1, 타입2, 타입3, ...) VALUES ( 값1, 값2, 값3, ... )
> INSERT INTO topic (title, description, created, author, profile) VALUES('MySQL', 'MySQL is ...', NOW(), 'me', 'developer');

* DESC 테이블이름;//해당 테이블의 구조보기

SELECT * FROM topic; //topic 테이블의 모든 데이터 보기
```