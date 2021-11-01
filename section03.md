# 익스프레스 (ExpressJS) 기초

### 익스프레스 (ExpressJS)
- 익스프레스란 Node.JS로 만들어진 웹 프레임워크이다. [공식 사이트](https://expressjs.com/)

### 어플리케이션
- 어플리케이션이란 익스프레스 객체(인스턴스)
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
