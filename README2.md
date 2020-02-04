# 관계형 데이터베이스

데이터의 중복을 최소화하기 위해 여러 개의 테이블을 사용함.

## 테이블 분리하기
```
RENAME TABLE topic TO topic_backup; //테이블 이름 바꾸기

// topic 테이블 생성
CREATE TABLE `topic` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `title` varchar(30) NOT NULL,
  `description` text,
  `created` datetime NOT NULL,
  `author_id` int(11) DEFAULT NULL,
  PRIMARY KEY (`id`)
);

// author 테이블 생성
CREATE TABLE `author` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `name` varchar(20) NOT NULL,
  `profile` varchar(200) DEFAULT NULL,
  PRIMARY KEY (`id`)
);
```

## 테이블 JOIN
```
SELECT * FROM topic LEFT JOIN author ON topic.author_id = author.id;

SELECT topic.id, title, description, name, profile FROM topic LEFT JOIN author ON topic.author_id = author.id;
(topic.id AS topic_id 로 표시되는 열 이름 변경 가능)


```