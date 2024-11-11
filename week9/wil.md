# 9주차 gdsc 스터디

## 1. 브라우저 캐싱

-요청 분류

1. 단순 조회 요청

:여러번 요청해도 결과 동일

:url에 정보를 넣어 전달해도 됨

:캐싱 가능

2. 새로운 리소스 생성 요청

:요청마다 결과 변경 가능

:민감한 정보를 다룸

:캐싱 불가능

## HTTP Method

이번 스터디에서는 주로 GET, POST 위주로 다룬다

1. GET: 웹 브라우저의 기본 Http Method

- 브라우저 캐싱 기능 지원
- 정보 읽기,검색 요청에 주로 사용됨
- url에 정보를 넣어 전달

2. POST:기본 지원 x

- 캐싱 기능 지원 x (멱등성 x)
- Request Body에 정보 들어감
- 새로운 요소 생성, 로그인 등에 사용됨

### 실습에서 질문 3 을 추가하기 위해서 해야 하는 것

http://localhost:8000/questions/create?subject=질문3&content=질문내용3

**Http Request**
목적지 : localhost:8000

경로 : /questions/create

정보 : subject=질문3

**start-line (시작 라인)**

=> GET /questions/create?subject=질문3 HTTP/1.1:

**header(헤더)**

:로그인 유지방식, 응답 양식, 언어 등 설정

### form, input

데이터를 입력받고 전송하기 위한 태그

Input 태그에서 데이터를 입력받을 수 있고, form 태그의 action 속성의 url로 전송한다.

form 태그의 method 속성을 post로 변경해 POST 방식으로 요청이 가능하다.
