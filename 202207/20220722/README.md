# 20220721


## JPA 무엇인가?

**Java Persisitence API**

- **JPA는  `자바 진영의 ORM 기술 표준` 이며, 어플리케이션과 JDBC 사이에서 동작**
- **ORM? 객체와 테이블을 매핑해서 `패러다임의 불일치를 개발자 대신 해결`해준다.**



## JPA 왜 사용해야 하는가?

- **INSERT SQL을 작성하고 JDBC API를 사용하는 지루하고 반복적인 일을 JPA가 대신 처리해준다.**
- **CREATE TABLE같은 DDL문 자동 생성**

<br></br>

**9조의 궁금증**

**JPA vs. Spring Data JPA vs. Hibernate vs. JDBC**

9조 팀 회의 전 각 팀원은 위 4개 키워드의 개념을 혼동하고 있었음.

그러나 팀 회의 과정에서 각각의 의미와 차이에 대해 궁금증을 갖게 됨

그 결과 위 4개는 전부 다른 개념임을 알게 됨

**정리**

1. **JPA?**   
   자바 진영의 ORM 기술 표준 명세이며, 인터페이스임   
       ** ORM(Object Relational Mapping)은 객체와 테이블을 매핑하는 기술
2. **Spring Data JPA?**   
   스프링에서 제공하는 모듈. 쉽게 말해, 개발자가 JPA를 더 쉽고 편하게 사용할 수 있도록 함
3. **Hibernate?**   
   JPA 인터페이스를 구현한 대표적인 오픈소스
4. **JDBC?**   
   자바에서 데이터베이스에 접속할 수 있도록 하는 자바 API







