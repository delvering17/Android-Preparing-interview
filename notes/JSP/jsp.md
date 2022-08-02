# JSP

---

## include와 forward의 차이

include : `<jsp:include page=”path”/>`

forward : `<jsp:forward page=”path”/>`

### 공통점

- request를 전달하는데 사용한다. 전달할 때 객체를 전달 할 수 있다.

### 차이점
requst의 제어권을 넘기는 방식이다.
- include는 ‘포함'이라는 뜻처럼, 현재 페이지에서 include를 한 url 페이지에게 제어권을 잠시 빌려주고 모든 처리가 끝나면 다시 현재 페이지에게 제어권이 돌아가게 된다. 이때 클라이언트 화면은 현재 페이지 속에 url 페이지가 포함되어 보여진다.
- forward는 현재 페이지에서 url 페이지로 forward하면 제어권을 넘겨주고 다시 현재 페이지는 전달받지 못한다. 클라이언트 화면은 현재 페이지의 처리화면은 보이지 않고 url 페이지의 처리 화면을 보게 된다.
- 
---

## cookie

- 쿠키는 디바이스에 파일형태로  저장된다.
- 웹 사이트에서 클라이언트의 정보를 저장하기 위해서 클라이언트의 디바이스에 저장하는 파일을 말한다. 특정 사용자에게 맞춤 광고를 보여주거나 최근 본 상품 같은 정보를 저장한다.
- JSESSIONID : 클라이언트가 로그인 했을 때 쿠키에 인증 정보를 넣는 것이 아닌 서버에 저장을 하고 관리하게 된다. 이때 클라이언트는 요청을 보낼 때 JSESSIONID을 보내서 서버는 그것을 가지고 클라이언트를 식별하여 응답한다.

## static page vs dynamic page

### static page 정적 페이지
-  파일 경로를 요청하면 Web Server는 동일한 경로를 찾아 해당 <File Contents>를 반환한다. 항상 같은 페이지를 반환하기 때문에 정적(static)이다.
  
### dynamic page 동적 페이지
-  파일 경로를 요청할 때 인자를 넘겨주면 WAS(Web application Server)는 인자에 따라 다른 페이지를 반환한다.
  
---
## Web Server vs WAS(Web Application Server)
  
### Web Server

- 하드웨어로는 Web server가 있는 컴퓨터를 말하고, 소프트웨어로는 client의 request를 받아서 static page, contents를 제공하는 프로그램이다.
- 기능 -정적인 컨텐츠는 WAS에 보내지 않고 바로 클라이언트에 제공하고, 동적인 컨텐츠는 WAS에 보낸다.
- 만약 정적인 컨텐츠를 WAS까지 보내게 되면 서버에 부담이 가므로 정적인 컨텐츠는 Web Server에서 빠르게 처리하는 것이다.
 ex) Apache Server, Nginx, IIS(Microsoft, Internet Information Server)

### WAS(Web Application Server)

- web Server같은 컨텐츠를 반환하지만, DB 등의 로직 처리를 필요로 하는 컨텐츠 위한 JSP, Servet을 다루는 서버이다. Web Server와 Web Container가 합쳐진 기능을 한다.
- 기능 - 프로그램 실행 환경과 DB 접속 기능 제공, 여러 개의 트랜잭션(논리적인 작업 단위) 관리 기능, 업무를 처리하는 비즈니스 로직 수행

ex) Tomcat, JBoss, Jeus, Web Sphere

- WAS는 client의 request 맞는 데이터를 그때그때 만들어서 제공한다.
  
---
  

  
