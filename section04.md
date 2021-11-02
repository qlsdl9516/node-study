# npm 에 대해 좀 더 알아보기

### npm
- <code>npm install</code> 명령어를 사용하여 외부 모듈 설치 
- node_modules 디렉토리에 설치됨

### 패키지 초기화
- <code>npm init</code> 명령어를 사용하여 package.json 생성  

  ![image](https://user-images.githubusercontent.com/92710241/139801861-d7d0317c-5119-46c1-9c3e-d9ea996eaba1.png)
- 생성된 package.json
   
  ```
    {
      "dependencies": {
      "express": "^4.17.1"
    },
    "name": "study",
    "version": "1.0.0",
    "main": "index.js",
    "devDependencies": {},
    "scripts": {
      "test": "echo \"Error: no test specified\" && exit 1"
    },
    "author": "",
    "license": "ISC",
    "description": ""
  }
  ```

### 패키지 관리
- <code>npm install [모듈명] --save</code> 명령어 실행 시 모듈 설치 후 package.json 파일의 dependencies에 버전 입력됨
- <code>npm install</code> 명령어 실행 시 package.json 파일의 dependencies을 참조하여 해당 모듈 설치

### 스크립트 사용
- package.json 파일의 script에 key를 추가하고 명령어를 입력
  ```
    {
      "dependencies": {
        "express": "^4.17.1"
      },
      "name": "study",
      "version": "1.0.0",
      "main": "index.js",
      "devDependencies": {},
      "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1",
        "start": "node index.js" // script 추가
      },
      "author": "",
      "license": "ISC",
      "description": ""
    }
  ```
  <code>npm start</code> 명령어 실행 시 <code>node index.js</code> 명령어 실행
