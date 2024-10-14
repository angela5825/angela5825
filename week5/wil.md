# 4주차 gdsc 스터디

## 1. 프로젝트와 어플리케이션의 개념

**프로젝트** : 우리가 장고로 만드는 소프트웨어 전체

**어플리케이션**: 프로젝트 내에서 기능별로 쪼개놓은 단위

-> 1 프로젝트 다 어플리케이션

## 2. DB와 Model- 장고는 class를 통해 DB테이블을 만든다.

- Models.py에 클래스를 생성하면, 장고가 클래스를 토대로 DB 테이블을 생성
- DB 테이블에서 값을 조회할 때 models.py에 만들어놓은 클래스의 객체에 값을 담아 반환

## 3. 장고 ORM 사용법

- 클래스이름.objects 를 이용해 DB에 저장된 값에 접근

- 클래스이름.objects.all() 사용 ->
  모든 테이블 정보를 객체로 만들어 리스트에 넣어 반환
- 클래스이름.objects.get() 사용 ->
  조건에 맞는 데이터를 객체로 만들어 반환

  ### 동적 html 생성

  (예시)

```
  def index(request):

  name= 'kim'

  context = {'name': name}

  return render(request,'index.html',context)
```

**render 함수**로 파일 경로 뒤에 html내에 넣고 싶은 정보를 딕셔너리에 담아 넘겨 줄 수 있다.

이 함수에서 사용되는 인자에 대한 설명

1. request= 장고에서 만들어서 넣어준 HTTP Request 객체
2. 'index.html' = 응답할 html 파일 이름
3. context = html 파일에서 사용할 딕셔너리

### CSS

- **h1,h2,h3** : 제목을 생성해주는 태그, 숫자가 낮아질 수록 폰트 크기가 작아짐
- **p** : Paragraph, 문단을 생성해주는 태그
  입력한 부분 앞 뒤로 빈 줄이 생기면서 텍스트 단락을 만들어줌
- **a** :하이퍼링크를 걸어주는 태그, href 속성안에 지정한 링크로 하이퍼링크가 연결된다.

  (예시)

  ```
  <a href='www.google.com'>google</a>
  ```

- **ul,ol,li** :목록(list)을 만들어주는 태그.

  ul,ol 태그 안에 li 태그를 넣어 목록을 만든다.

  - ul (unordered list)는 순서가 없는 목록
  - ol (ordered list)는 순서가 있는 목록을 만들어준다

## 4. 장고 template

장고는 HTML을 동적으로 생성할 수 있다.

태그를 만들수는 없음, 태그 안의 내용을 동적으로 바꿔주기 가능

#### 사용법

render 함수 마지막 인자에 원하는 데이터를 담은 딕셔너리를 넣어준다.
