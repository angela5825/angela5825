## 7주차

#### 관계형 데이터베이스 시스템(RDBMS)

- RDB(관계형 데이터베이스)는 row 단위로, 다른 row들을 구별할 수 있어야 함
- **pk(primary key)**

  1. 중복되지 않아야 함
  2. 잘 변경되지 x
  3. 모든 row가 값을 가질 수 있도록 (not null)

- **foregin key 외래키**
  (ex) 맥도날드 주문할 때 한 사람이 매우 많이 주문 -> 이름이 바뀜

  - 회원정보와 주문정보를 구분해서 저장한다.(테이블을 나눈다)

- (ex) 당근 마켓:DB에 저장해야 할 것이 많다 <- 복잡하게 얽혀 있기 때문에

#### Relate

- **일대일( 1: 1 ) 관계**

  (ex) 학생 한 명당 1개의 사물함이 배정된다면, 1개의 사물함은 학생 1명만 사용 가능

      - 테이블을 나눈다, FK를 이용해 두 테이블을 하나씩 연결 (이유) 사물함이 없는 학생도 존재하기 때문에 (사물함 번호,위치에 null)

      -> 데이터를 관리하기 어렵다 : data에 null이 없는 것이 좋다.

- **일대다 (1: N) 관계**

  (ex) 회원 한 명이 여러 개의 주문이 가능 -> 주문이 가질 수 있는 주문자는 1명 뿐

      - FK를 이용해 두 테이블을 하나씩 연결 -> 일대다에서 "다"쪽의 테이블이 FK를 가짐

- **다대다 (N : M) 관계**

  (ex) 학생 1명은 여러 개의 강의를 수강할 수 있고 한 강의는 여러 명의 학생이 신청할 수 있다

      - 보조 테이블을 만들어서 관계를 표현함

#### 게시판 글에 댓글을 달 수 있다면 게시판 과 댓글의 관계

    **(A) 1: 다**
