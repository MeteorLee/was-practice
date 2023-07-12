# 웹 개발 연습 프로젝트

## 사용 도구

- java 17
- gradle 8.0
- intellij
- git

## 라이브러리

- assertj 3.23.1
- logback 1.2.3


## STEP

- Step1 : 사용자 요청을 메인 Thread가 처리하도록 한다.
- Step2 : 사용자 요청이 들어올 때마다 Thread를 새로 생성해서 사용자 요청을 처리하도록 한다.
- Step3 : Thread Pool을 적용해 안정적인 서비스가 가능하도록 한다.

# 서블릿 프로그래밍

## CGI 프로그래밍과 서블릿

### CGI

CGI(Common Gateway Interface)
- 웹 서버와 애플리케이션 사이에 데이터를 주고받는 규약
- CGI 규칙에 따라서 만들어진 프로그램을 CGI 프로그램이라고 함
- CGI 프로그램 종류로는 컴파일 방식(C, C++, Java 등)과 인터프리터 방식(PHP, Python 등)이 있음

#### 서블릿과 서블릿 컨테이너

웹 서버 <-> Servlet Container <-> Servlet 파일

#### 인터프리터 방식 CGI 프로그램

웹 서버 <-> Script engine <-> Script 파일

### Servlet (Server + Applet의 합성어)

- 자바에서 웹 애플리케이션을 만드는 기술
- 자바에서 동적인 웹 페이지를 구현하기 위한 표준

### Servlet Container

- 서블릿의 생성부터 소멸까지의 라이프사이클을 관리하는 역할
- 서블릿 컨테이너는 웹 서버와 소켓을 만들고 통신하는 과정을 대신 처리해준다. 개발자는 비지니스 로직에만 집중하면 된다.
- 서블릿 객체를 싱글톤으로 관리 (인스턴스 하나만 생성하여 공유하는 방식)
  - 상태를 유지(stateful)하게 설계하면 안됨
  - Thread safety 하지 않음

### WAS vs 서블릿 컨테이너

- WAS는 서블릿 컨테이너를 포함하는 개념 (거의 동일하다고 생각해도 됨)
- WAS는 매 요청마다 스레드 풀에서 기존 스레드를 사용함
- WAS의 주요 튜닝 포인트는 max thread 수
- 대표적인 WAS로는 톰캣이 있다.














