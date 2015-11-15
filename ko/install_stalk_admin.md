Install and start STALK Admin Server
======================
`STALK Admin Server` 는 웹사이트 관리자가 고객과 실시간 대화하고 통계 등의 기능을 제공하는 관리용 시스템입니다.

`XPUSH-CHAT`서버와는 별도로 실행되는 서버입니다.

### 1. STALK Admin Server 소스 다운로드 및 설치
``` bash
  $ git clone https://github.com/xpush/io.stalk.admin.git
  $ cd io.stalk.admin
  $ bower install
  $ npm install
```

### 2. 설정 파일 작성하기
`STALK Admin Server` 서버를 실행하기 위해서는 mongodb 의 주소와 `XPUSH-CHAT` 의 Session 서버 주소와 Application 명을 설정해야 합니다.
``` bash
  $ vi config.json

  module.exports = {

    // MongoDB connection options
    mongo: {
      uri: 'mongodb://127.0.0.1/STALK'
    },

    // Session Server url of XPUSH
    xpush: {
      url: "http://127.0.0.1:8000",
      A: "STALK"
    }
  };

```  

### 3. STALK Admin Server 실행하기.
``` bash
  $ grunt serve --config ./config.js
```
