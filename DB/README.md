# SQL 명령어

<h2> DDL, DML, DCL에 대해 </h2>

### DDL
---
> * DATA DEFINITION LANGUAGE
> 
> * 테이블의 구조, 관계 생성
> ```
> CREATE(DB, 테이블 생성), DROP(DB, 테이블 제거), TRUNCATE(데이터 제거), ALTER(열 변경)
> ```
> #### DDL의 제약 조건 유형
> ```
> PRIMARY KEY(기본키 정의), FOREIGN KEY(외래키 정의), UNIQUE(유일한 값 지정),
> NOT NULL(NULL 지정 불가), CHECK(개발자 정의 제약 조건)
> ```

### DML
---
> * DATA MANIPULATION LANGUAGE
> 
> * 테이블 데이터의 검색, 등록, 수정, 삭제
> ```
> SELECT(행 검색), UPDATE(행 수정), DELETE(행 제거), INSERT(행 삽입) 
> ```
> #### SELECT 문의 OPTION
> ```
> ALL(중복을 포함한 조회 결과 출력), DISTINCT(중복을 제거한 조회 결과 출력)
> ```

### DCL
---
> * DATA CONTROL LANGUAGE
> 
> * 데이터의 보안, 무결성, 회복, 병행 수행제 등을 정의
> ```
> GREANT(사용자 권한설정), REVOKE(사용자 권한해제)
> ```
>
> ### TCL( DCL )
> ---
> * TRANSACTION CONTROL LANGUAGE
> 
> * DB적용 전의 일종의 인터페이스
> ```
> COMMIT(트랜잭션의 결과를 물리적 디스크의 DB에 저장),
> ROLLBACK(트랜잭션의 결과를 포인트 지점으로 복구시킴),
> CHECKPOINT(트랜잭션의 복귀지점을 설정)
> ```
> 
> * ROLLBACK의 사용 예시
> ```
> savepoint A;
> SELECT * FROM ...
> savepoint B;
> ROLLBACK A; -- savepoint A까지 결과를 되돌림
> ROLLBACK B; -- savepoint B까지 결과를 되돌림
>```
> * commit; 명령어를 통해 물리적 저장소에 트랜잭션 결과를 적용시킴