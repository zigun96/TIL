# SQL 명령어

## DDL, DML, DCL

### DDL
---
* DATA DEFINITION LANGUAGE

* 테이블의 구조, 관계 생성
```
CREATE(DB, 테이블 생성), DROP(DB, 테이블 제거), TRUNCATE(데이터 제거), ALTER(열 변경) ...
```

### DML
---
* DATA MANIPULATION LANGUAGE

* 테이블 데이터의 검색, 등록, 수정, 삭제
```
SELECT(행 검색), UPDATE(행 수정), DELETE(행 제거), INSERT(행 삽입) ...
```

### DCL
---
* DATA CONTROL LANGUAGE

* 데이터의 보안, 무결성, 회복, 병행 수행제 등을 정의
```
GREANT(사용자 권한설정), REVOKE(사용자 권한해제)
```
### DCL의 TCL
---
* TRANSACTION CONTROL LANGUAGE

* DB적용 전의 일종의 인터페이스
```
COMMIT(트랜잭션의 결과를 물리적 디스크의 DB에 저장),
ROLLBACK(트랜잭션의 결과를 포인트 지점으로 복구시킴)
```

* ROLLBACK의 사용 예시
```
savepoint A;
SELECT * FROM ...
savepoint B;
ROLLBACK A; -- savepoint A까지 결과를 되돌림
ROLLBACK B; -- savepoint B까지 결과를 되돌림