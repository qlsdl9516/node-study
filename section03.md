# 익스프레스 (ExpressJS) 기초

### 익스프레스 (ExpressJS)
- 익스프레스: Node.JS로 만들어진 웹 프레임워크 ([공식 사이트](https://expressjs.com/))

### 어플리케이션
- 어플리케이션: 익스프레스 객체(인스턴스)
```
const express = require('express');
const app = express(); // app이 어플리케이션 객체
```
- 어플리케이션의 역할
  1. 서버에 필요한 기능인 미들웨어 추가
  2. 라우팅 설정
  3. 서버를 요청 대기 상태로 생성
  ```
    app.listen(3000, function() {
    console.log('Server is running');
    })
  ```
  
### 미들웨어
- 미들웨어: 함수들의 연속 (use 함수를 사용하여 미들웨어 추가)
  ```
    function logger(req, res, next) { // 미들웨어 인터페이스는 정해져 있음 (requset, response, next)
      console.log("i am logger");
      next(); // 미들웨어 함수는 마지막에 다음 함수를 실행 시키기 위하여 next 함수를 호출해야 함. 
    }
    
    function logger2(req, res, next) {
      console.log("i am logger2");
      next(); 
    }
    
    app.use(logger) // use라는 함수를 사용하여 logger 미들웨어 추가
    app.use(logger2)
  ```
