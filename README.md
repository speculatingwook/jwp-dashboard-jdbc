# JDBC 라이브러리 구현하기


> 나만의 JDBC 라이브러리를 만들어보자.

## 💻 기능 요구 사항

### 1단계 - JDBC 라이브러리 구현하기

- [ ]  직접 DataSource를 이용해 UserDao를 구현한다.
- [ ]  반복 로직을 JdbcTemplate으로 이동 시키고, 이를 이용해 UserDao를 구현한다.
- [ ]  항상 UserDaoTest의 모든 테스트 케이스는 통과해야한다.

### 2단계 - 리팩터링 힌트

> 자바가 제공하는 기능을 극한으로 활용해 클린 코드를 작성하는 연습을 한다.

- [ ]  익명 클래스, 함수형 인터페이스, 제네릭, 가변 인자, 람다, try-with-resources, checked vs unchecked exception 등을 활용한다.

![image](https://user-images.githubusercontent.com/45311765/194697540-2027c7b5-9592-4c39-b590-6cfd46d664d8.png)

### 3단계 - 트랜잭션 적용하기

-  트랜잭션 경계를 설정한다.
    - [ ]  트랜잭션 시작, 커밋, 롤백 시점을 설정한다.
-  트랜잭션 동기화를 적용한다.
    - [ ]  스프링의 TransactionMannager를 이용해 Connection을 받아온다.
-  트랜잭션 서비스를 추상화한다.
    - [ ]  트랜잭션 서비스(TxUserService)와 애플리케이션 서비스(AppUserService)가 분리되어 있다.
-  트랜잭션 롤백이 적용 되어 UserServiceTest 클래스의 testTransactionRollback() 테스트 케이스가 통과한다.