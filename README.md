# Front End

## Client - Server Model

https://ko.wikipedia.org/wiki/%ED%81%B4%EB%9D%BC%EC%9D%B4%EC%96%B8%ED%8A%B8_%EC%84%9C%EB%B2%84_%EB%AA%A8%EB%8D%B8

https://darvishdarab.github.io/cs421_f20/docs/readings/restful/api/

- 클라이언트-서버모델에서 클라이언트와 서버는 일대일 가상 연결 개념
- 클라이언트의 request(요청)과 서버의 response(응답)의 사이클로 통신이 이루어짐

## Front End VS Back End

- Front End
  - 사용자와 직접 대명하는 화면관련 개발
  - 서버에 저장된 F.E(Front End) 소스코드는 처리되지 않고 클라이언트로 전송
  - 클라이언트에서 실행되고 있는 브라우저가 FE 소스코드를 처리(랜더링)해서 화면에 표시
  - 클라이언트에서 실행되는 브라우저 종류
    - 크롬, 엣지, 파이어폭스 등
- Back End
  - 서버에서 처리하는 데이터 및 데이터 베이스, 보안등 화면에 보이지 않는 것을 개발
  - 서버에 저장된 B.E(Back End) 소스코드는 서버에서 처리(컴파일)
  - 처리된 데이터 결과가 클라이언트로 전송
  - 서버에서 실행되는 소프트웨어
    - apache(리눅스), IIS(윈도우) 등
