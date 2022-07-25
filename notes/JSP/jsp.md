# JSP

## include와 forward의 차이

include : `<jsp:include page=”path”/>`

forward : `<jsp:forward page=”path”/>`

### 공통점

- request를 전달하는데 사용한다. 전달할 때 객체를 전달 할 수 있다.

### 차이점
requst의 제어권을 넘기는 방식이다.
- include는 ‘포함'이라는 뜻처럼, 현재 페이지에서 include를 한 url 페이지에게 제어권을 잠시 빌려주고 모든 처리가 끝나면 다시 현재 페이지에게 제어권이 돌아가게 된다. 이때 클라이언트 화면은 현재 페이지 속에 url 페이지가 포함되어 보여진다.
- forward는 현재 페이지에서 url 페이지로 forward하면 제어권을 넘겨주고 다시 현재 페이지는 전달받지 못한다. 클라이언트 화면은 현재 페이지의 처리화면은 보이지 않고 url 페이지의 처리 화면을 보게 된다.
