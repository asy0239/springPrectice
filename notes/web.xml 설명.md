# web.xml 설명

## web.xml은 서버 (WAS)가 운영하기 위한 내용을 작성

- 자바 기반의 웹 애플리케이션이라면 무조건 있어야 함 (jsp/spring/...)
- xmlns : xml name space 의 줄임말, 태그 정보를 제공

### 전역(global) 설정 파일을 지정( context-param 태그)

- 스프링 전체에 영향을 미치는 설정
- 이름은 무조건 contextConfigLocation 이라고 작성
- 요청처리와 상관없는 설정이 들어감
- 데이터베이스 or 이메일 발송 등 ...

### Spring 에서 사용자의 모든 요청을 처리하는 핵심(core) 서블릿 = 중앙 제어 서블릿(servlet 태그)

- 요청처리 교통정리, 콜센터, 분배기 개념
- 만드려면 난이도가 너무 높아서 스프링에서 사용하도록 만들어서 제공
- 이름 : appServlet
- 클래스 : org.springframework.web.servlet.DispatcherServlet
- 초기 설정 : 
  - 설정파일 : servlet-context.xml 
- mapping pattern(url-pattern 태그) :
  - / : 전부다(원한다면 제외 할 수 있음, 나머지 전부 다)
  - /* : 전부다(하나도 빠짐없이)
  - *.me : 위치 상관없이 .me 로 끝나는 주소

### 여러개로 나누어진 설정파일들을 연결해주는 도구 (listener 태그)

### 단, 반드시 전역 설정(root-context.xml)이 서블릿 설정보다 상위에 존재한다.



