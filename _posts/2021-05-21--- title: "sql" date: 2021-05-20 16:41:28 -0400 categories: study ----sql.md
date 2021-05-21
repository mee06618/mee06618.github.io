---
title: "sql"
date: 2021-05-21 16:41:28 -0400
categories: study
---
  ## sql
  - 데이터베이스 생성
    - CREATE DATABASE [database name] CHARACTER SET [character set];
  - 데이터베이스 선택
    - USE [database name];
  - 데이터베이스 삭제
    - DROP DATABASE [database name];
  - 테이블 생성
    - CREATE TABLE [table name] ([column1 name][datatype], …);
  - 테이블 삭제
    - DROP TABLE [table name];
  - 테이블에 필드(열) 추가
    - ALTER TABLE [table name] ADD [column name][datatype];
  - 테이블 필드(열) 타입 변경
    - ALTER TABLE [table name] MODIFY COLUMN [column name][datatype];
  - 테이블 필드(열) 삭제
    - ALTER TABLE [table name] DROP [column name];
  - 테이블에 레코드(행) 추가
    - INSERT INTO [table name] VALUES (value1, value2, value3…);
  - 테이블의 레코드(행) 선택
    - SELECT * FROM [table];
  - 테이블의 레코드(행) 내용 수정
    - UPDATE [table] SET [column]=[value] WHERE [condition];
  - 테이블의 레코드(행) 삭제
    - DELETE FROM [table] WHERE [condition];
  - Join 기본 문법
    - SELECT
    테이블이름.조회할 테이블,
    테이블이름.조회할 테이블
    FROM 기준테이블 이름
    (INNER, LEFT, RIGHT FULL) JOIN 조인테이블 이름
    ON 기준테이블이름.기준키 = 조인테이블이름.기준키;
## 자주 하는 실수
  - 까먹음
## 큐
  - sql매우중요
## 내가 모르는 것
  - 까먹었던내용
## 느낀점
  - 다시 해야겠다 너무 까먹음
