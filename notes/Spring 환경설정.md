# Spring 환경설정

1. STS 설치
   - 4버전과 3버전이 있는데 목적에 따라 버전을 선택을 해서 진행해야함
   - STS download 검색해서 운영체제에 따라 맞게 다운 진행
2. 환경변수 설정
   - 자바 환경변수와 동일하게 설정을 해주면된다. 
3. STS tool 실행
   - 인코딩 설정, context type -> java class file , text -> utf-8
   - workspace, css, html, jsp, json, xml, spelling 모두 utf-8 로 진행
   - preferences -> java -> compiler -> 버전 맞추기 -> installed jres -> add 사용할 버전 추가
4. 서버 설정
   - tomcat을 사용할 것이므로 기존 vm 서버는 삭제후 tomcat 추가
5. legacy project  생성
   - pom.xml 의 자바 버전과 spring framework 의 버전을 맞추어야함
   - pop.xml은 maven 을 사용한다.
6. maven 설치
   - maven download -> 다운로드
   - 파일 경로 (bin 전까지) 환경변수에 추가
7. maven 연동
   - settings.xml 수정 -> 기본 다운로드 위치 설정
   - preferences -> user setting -> browse 로 settings.xml 을 선택하고 update
   - installations -> add -> maven 위치 경로 , 근데 기본 maven이 있어 해도되고 안해도된다.