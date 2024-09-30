## week2 수업 내용 정리- 9/23

#### **장고 프로젝트-분업화: MTV패턴**

1. Model : 데이터 입출력
2. Template
3. View

#### **장고 프로젝트 명령어**

1. django-admin startproject
2. django-admin startapp
3. python manage.py runserver
4. python manage.py makemigrations
5. python manage.py migrate

-> 1,2번 중요

#### 프로젝트 vs 어플리케이션

**프로젝트**는 우리가 장고로 만드는 소프트웨어 전체

**어플리케이션**은 프로젝트 내에서 기능별로 쪼개놓은 단위

**하나의 프로젝트는 보통 여러게의 어플리케이션으로 이루어짐**

#### 장고 프로젝트의 구조에 대해서

User -> **urls.py** (view목적지 찾아 전달) -> **view.py(흐름 제어)** -> **templates**(응답 내용 관리)

**models.py**(데이터 저장,검색관리) <-> **view.py**

---

#### 실습 진행
