## SQL문 종류
|                종류               |         역할        |  
| -------------------------------- | :----------------: |  
| DML(Data Manipulation Language)  |    데이터 조작       |  
| DDL(Data Definition Language)    |   데이터 정의        |  
| DCL(Data Control Language)       |   데이터베이스 제어   |  

#
## SQL로 할 수 있는 것들
1. 검색  
2. 정렬 및 연산  
3. 추가, 삭제, 갱신  

#
## 실무에서 자주 쓰는 명령은 데이터 조작어(DML)
- SELECT : Database에서 원하는 데이터를 **추출(조회)**
- UPDATE : Database에서 데이터 **업데이트**
- INSERT INTO : 새로운 데이터를 Database에 **삽입(추가)**
- DELETE : Database에서 데이터 **삭제**

#
## SELECT
: 특정 데이터 추출(조회)  
-> `SELECT {특정 컬럼} FROM {특정 테이블};`  
  
```sql
select * from Users;
```
-> `Users` 라는 테이블에서 모든 컬럼을 조회하겠다.  
  
```sql
select name from Users;
```
-> `Users` 라는 테이블에서 `name` 컬럼을 조회하겠다.  
  

#
## WHERE (조건문)
: 데이터를 특정할 때 사용하는 식
- `=` : 같다
- `>` : 보다 큰
- `<` : 보다 작은
- `>=` : 보다 크거나 같은
- `<=` : 보다 작거나 같은
- `<>` : 같지 않은
- `between a and b` : a 와 b 사이의 값 (a 이상 b 이하)
- `in` : `or` 과 비슷, 한번에 여러개의 값 확인하고 싶을 때
```sql
select * from Users where name = 'jsoh';
```
-> `Users` 라는 테이블에서 `name`이 `jsoh`인 값만 조회하겠다.  

```sql
select * from Users where age > 29;
```
-> `Users` 라는 테이블에서 `age`가 `30이상`인 값만 조회하겠다.  
