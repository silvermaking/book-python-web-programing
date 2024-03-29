# LInk 

- 깃허브 예제 소스 파일([링크](https://github.com/Baepeu/python_web_programming_django3))
- 파이썬 웹 프로그래밍 책([링크](http://www.yes24.com/Product/Goods/69758579?OzSrank=1))



# Project

|             Chapter              |         content(.md)          |         project         |
| :------------------------------: | :---------------------------: | :---------------------: |
|        ch2. 장고 시작하기        | [go](./django_default/ch2.md) | [go](./django_default/) |
| ch3. 튜토리얼 따라하기(설문조사) |     [go](./polls/ch3.md)      |     [go](./polls/)      |
|                                  |                               |                         |



# 1. 웹 프로그래밍이란?

## 1.1 인터넷과 웹 사이트

### **웹 사이트(Web site)**

- 도메인 이름이나 IP 주소, 루트 경로만으로 이루어진 일반 URL을 통하여 보이는 웹 페이지(Web Page)들의 의미 있는 묶음

### 도메인 주소

- www.google.com과 같은 형태
- 도메인 주소와 연결되어 있는 IP주소를 찾아서 해당 IP주소를 가진 컴퓨터로 접속
- DNS(Domain Name System)
  - 도메인 주소와 IP주소를 연결시켜주는 전화번호부와 같은 개념

## 1.2 웹 프로그래밍의 세계

웹 프로그래밍은 웹 사이트 혹은 웹 페이지를 만드는 과정

- 웹 브라우저 단: HTML, CSS, JavaScript
- 서버 단 : Python, Ruby, PHP, Java

### 프론트엔드

- 브라우저 단에서 동작하는 코드를 작성하는 것
- 클라이언트 사이드 프로그래밍
- HTML : 페이지의 구성, 뼈대를 담당
- CSS : HTML 요소에 색상, 크기 등 디자인적인 요소를 적용
- JavaScript : 이미 만들어진 페이지의 내용을 변경하거나 페이지 구성물들에 움직임을 부여

### 백엔드

- 서버쪽에서 실행되는 코드를 작성하는 것
- 서버 사이드 프로그래밍
- 수 많은 언어 사용 가능

### 웹 프레임워크

- 풀스택(FullStack) 프레임워크
  - 웹 서비스를 만드는 데 필요한 다양한 기능(DB, dlswmd, 템플릿, 엔진 등)을 모두 포함하고 한꺼번에 설치하는 형태
  - Spring, Django 등
- 마이크로(Micro) 프레임워크
  - 가볍고 빠르다
  - 기능 개발에 비교적 시간이 오래 걸린다.
  - Sinatra, Flask 등

## 1.3 웹 서버와 웹 애플리케이션 서버

### 웹 서버

- 다양한 기능을 하는 각각의 소프트웨어가 동작할 수 있는 환경이 되는 컴퓨터
- 웹 서버 프로그램
  - 사용자가 브라우저를 통해 서버에 접속했을 때 요청을 정리하고 웹 애플리케이션으로 전달하는 역할을 하는 프로그램
  - 기존에는 CGI(Common Gateway Interface) 방식 사용
  - 웹 애플리케이션 서버 방식으로 발전
  - Java : 톰캣
  - 파이썬 장고, 루비 레일즈 : Gunicorn 방식의 미들웨어 서버 방식

### 웹 애플리케이션 서버

- 웹 서비스 자체가 돌아가는 서버

## 1.4 장고

WSGI라는 미들웨어 방식으로 웹 애플리케이션 서버를 구동해 적은 리소스로 높은 효율성을 내기 위해 발전해가고 있다.

## 1.5 인프라라 불리우는 것들에 대해서

### 인프라란

- 다양한 종류의 서버 컴퓨터들이 동작하는 환경과 이 환경의 형태
- 클라우드 컴퓨팅 : 이런 인프라를 가상화를 통해 구성
- CDN, 로드밸런서 - 웹 서버 - (캐시, DB, 파일) 서버 들이 하나로 뭉쳐있는 형태

**CDN(Content Delivery Network)**

- 전세계 곳곳에 노드 컴퓨터를 두고 사용자가 필요한 데이터를 미리 저장해 놓거나 요청받은 이후에 다음 사용자를 위해 저장해 놓는 형태
- 서버와 사용자간 물리적 거리로 인한 응답 시간 증가를 최소화하기 위한 서비스
- 유튜브처럼 대용량 데이터를 전송해햐 하는 서비스에 사용

**로브밸런서**

- 여러 대의 서버 컴퓨터가 분산처리(아웃스켈일링)하여 서버의 로드율 증가, 부하량, 속도저하 등을 고려하여 적절히 분산처리하여 해결해주는 서비스

**웹 서버**

- 실제 요청을 처리하는 컴퓨터

**캐시 서버**

- 들어온 요청에 대한 응답을 미리 파일이나 메모리 캐시로 저장해 두는 컴퓨터
- Redis, Memcached

**데이터베이스**

- 컴퓨터에서 사용하는 엑셀과 비슷한 역할
- 데이터 관리 전용 서비스
- 데이터를 빠르게 저장하고 검색하는 용도

**파일 서버**

- 사용자가 업로드한 파일을 여러 사용자가 함께 봐야하는 경우 사용하는 서비스(예 : 인스타)
- 중앙에 하나의 이미지 서버를 준비해두고 이 곳을 통해 이미지를 공유하는 방식

## 1.6 파이썬과 장고

- 구글 앱 엔진에서 장고를 채용한 일로 유명해지기 시작했다.(지금은 구글 클라우드 내에서 서비스)
- 어떤 형태로 파이썬을 활용하던지 웹 서비스가 붙어야 한다.
- 장고는 파이썬 기반 웹 프레임워크
- 가장 빠른 시간내에 웹 서비스를 구현할 수 있는 프레임워크(생산성)
- ORM방식을 통해 데이터베이스를 다룰 수 있다.
- CRUD 기능을 제네릭 뷰라는 형태로 미리 구현되어 있다.
- 다양한 기본 미들웨어를 사용해 웹 애플리케이션 보안성이 높다.
