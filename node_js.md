# node js 기본기
### npm(node package manager)  
- 필요한 tool이 있으면 가져다가 다운받아서 사용하는 것이다.
- 프레임워크나 자바스크립트로 구현된 다양한 것을 다운 받아서 쓸 수 있다.
  
  > 사용 방법
  > - 터미널에서 npm install (모듈이름)
  ```
  npm install express
  ```
  => express라는 모듈을 다운 받은 상태임
  
  #### 예제
  
  ```
  const express = require('express')
  const app = express()

  app.get('/', function (req, res) {
  res.send('Hello World')
  })

  app.listen(3000)
  ```

  ### port 란?
  app.listem(port, () => {}

            *포트번호*
  => 몇번 포트에대해서 듣고 있다.

  - 항구의 선착장의 배가 들어갈 수 있는 정해진 번호
    => 들어올 수 있는 입구

    - 요청시 서버에 그냥 들어가는게 아니라 기본적으로 포트가 열려있어 특정 포트로 들어간다.
      ex) 서비스 포트는(상담원 연결은 1번, 문자상담은 2번) ARS 내선번호 IP는 대표전화번호 (XXX-XXX)

      ex) 80port : HTTP , 443port : HTTPS

      => 한 서버 내에서 여러 개 사용이 가능하다
  
  ### HTTP 메소드, 라우팅, 콜백함수
    ```
    app.get('/', (req, res) => {
      res.send('hello world!')
    })
    ```
    #### HTTP 메소드
    - Request(요청) -> Response(응답)
      => 요청의 목적, 종류를 알리는 수단
      ex) get - 주소창 데이터 전달 post - 내부적으로 body에 데이터 전달
    #### 라우팅 : '/'
    ex) https://www.youtube.com/watch?v=zl5b-DAutK
  
    => 라우팅에 따라서 보여지는 웹페이지가 달라진다

      ```
      / : 기본페이지
      /about : 소개하는 페이지
      /board : 게시판 페이지
      /board/write : 게시판 작성글 페이지
      ```

    #### 콜백함수 (callback)
    - 함수(끝나고 실행할 함수)

    ```
    setTimeout(()=>{console.log("1초")},1000)
    //setTimeout 함수 진행 후, 1초동안 잠시 대기 후 console.log 함수를 실행해라
    ```
    => 함수 실행 순서를 지정해준 느낌?
  
    
