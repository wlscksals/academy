# SQL 기본 CRUD

## DDL
> 데이터 정의어란?

데이터 베이스를 정의하는 언어,데이터를 생성,수정,삭제하는 등의 데이터의 전체의 골격을 결정하는 역할 <br>

* **create** : 데이터베이스,테이블 등을 생성
* **alter** : 테이블을 수정
* **drop** : 데이터베이스, 테이블을 삭제
* **truncate** : 테이블을 초기화

※ SCHMA,DOMAIN,TABLE,VIEW,INDEX를 정의하거나 변경 또는 삭제할 때 사용하는 언어
※ 데이터 베이스 관리자나 데이터베시이스 설계자가 사용
<br>
<br>
## DML
> 데이터 조작어란?

정의된 데이터 베이스에 입력된 러코드를 조회,수정,삭제한느등의 역할

* **select** : 데이터 조회
* **insert** : 데이터 삽입
*  **update** : 데이터 수정
*  **delete** : 데이터 삭제

※ 데이터베이스 사용자가 응용 프로그램이나 질의어를 통하여 저장된 데이터를 처리하는데 사용하는 언어
※ 데이터 베이스 사용자와 데이터베이스 관리 시스템 간의 인터페이스 제공

<br>
<br>

## DCL
> 데이터베이스에 접근하거나 객체에 권한을 주는등의 역할을 하는 언어

* **grant** : 특정 데이터베이스 사용자에게 특정 작업에 대한 수행권한을 **부여**
* **revoke** : 특정 데이터베이스 사용자에게 특정 작업에 대한 수행권한을 **박탈,회수** 
* **commit** : 트랜잭션의 작업을 **저장**
* **rollback** : 트랜잭션의 작업을 **취소,원래대로 복구**
<br>

**ROLL 객체** <br>
※ROLE 종류
CONNECT : DB 접속 권한
RESOURCE : 테이블이라든지 인덱스라든지 생성할 수 있는 권한
CREATE VIEW : 뷰 생성 권한
DBA : 모든 권한(관리자)

<br>
<br>

## **실습**

입력: mysql -u root -p

(testdb: db이름)<br>

**DB 조회**  <br>
show databases
<br>
<br>

**DB 위치 지정**  <br>
ues mysql
<br>
<br>

**DB생성** <br>
create database testdb; <br>
show databases; <br>

**테이블 확인**  <br>
show tables;  <br>
select * from user;   (user : table 이름)

|Tables_in_testdb|
|-|
|tbl_user   |

<br>
<br>

**Table생성** <br>
use testdb; <br>
show tables; <br>
cret table tbl_user( <br>
user_id varchar(10) primary key, <br>
user_password varchar(100) not null, <br>
user_name vartchar(45) not null); 
<br>
mysql> desc tbl_user; (tbl_user 테이블 확인하기) 
|Field|Type| Null |Key|Default| Extra |
|-|-|-|-|-|-|
| user_id       | varchar(10)  | NO   | PRI | NULL    |       |
| user_password | varchar(100) | NO   |     | NULL    |       |
| user_name     | varchar(45)  | NO   |     | NULL    |       |
<br>
<br>

**컬럼 추가(alter asdd)** <br>
alter table tbl_useradd column user_tel varchar(30) null after user_name ;
<br>

| Field         | Type         | Null | Key | Default | Extra |
|-|-|-|-|-|-|
| user_id       | varchar(10)  | NO   | PRI | NULL    |       |
| user_password | varchar(100) | NO   |     | NULL    |       |
| user_name     | varchar(45)  | NO   |     | NULL    |       |
| user_tel      | varchar(30)  | YES  |     | NULL    |       |
<br>
<br>

**컬럼 삭제(alter - dorp)** <br>
alter table tbl_user drop user_password;
<br>

| Field     | Type        | Null | Key | Default | Extra |
|-|-|-|-|-|-|
| user_id   | varchar(10) | NO   | PRI | NULL    |       |
| user_name | varchar(45) | NO   |     | NULL    |       |
| user_tel  | varchar(30) | YES  |     | NULL    |       |

<br>
<br>
**컬럼 수정(alter change)** <br>
alter table tbl_user change column user_tel user_phone varchar(100) not null;
<br>

| Field      | Type         | Null | Key | Default | Extra |
|-|-|-|-|-|-|
| user_id    | varchar(10)  | NO   | PRI | NULL    |       |
| user_name  | varchar(45)  | NO   |     | NULL    |       |
| user_phone | varchar(100) | NO   |     | NULL    |       |

<br>
<br>

**값 삽입( insert )** <br>
select * form tbl_user; <br>
insert into testdb.tbl_user(user_id,user_name,user_phone) values('user10','홍길동','010-222-3333'); <br>
insert into testdb.tbl_user values('user20','남길동','010-555-6666'); <br>

| user_id | user_name | user_phone   |
|-|-|-|
| user10  | 홍길동    | 010-222-3333 |
| user20  | 남길동    | 010-555-6666 |

<br>
<br>
**갑 수정( update )** <br>
update tnl_user set user_name ='철수' where user_id = 'user20'; <br>

| user_id | user_name | user_phone   |
|-|-|-|
| user10  | 홍길동    | 010-222-3333 |
| user20  | 철수      | 010-555-6666 |

<br>
<br>
**값 삭제( delete )** <br>
delete from tbl_user where user_id ='user10'; <br>

| user_id | user_name | user_phone   |
|-|-|-|
| user20  | 철수      | 010-555-6666 |

