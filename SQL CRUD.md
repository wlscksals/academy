# SQL 기본 CRUD

(testdb: db이름)

**DB 조회** 
show databases
<br>
**DB 위치 지정** 
ues mysql

**테이블 확인** 
show table;  
select * from user;

**DB생성**
create database testdb;
show databases;

**Table생성**
use testdb; 
show tables;
cret table tbl_user(
user_id varchar(10) primary key,
user_password varchar(100) not null,
user_name vartchar(45) not null);

