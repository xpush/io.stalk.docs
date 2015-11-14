Installation and Startup
======================
`STALK`는 총 3가자의 프로젝트로 구성되어 있습니다.
 * **xpush-chat**: 관리자와 고객이 서로 채팅할 수 있도록 연결하는 실시간 메시징 서버입니다. - [https://github.com/xpush/xpush-chat](https://github.com/xpush/xpush-chat)
 * **io.stalk.admin**: 관리자가 로그인한 후 고객과 대화 하거나 접속 통계를 확인하는 관리자 시스템입니다. - [https://github.com/xpush/io.stalk.admin](https://github.com/xpush/io.stalk.admin)
 * **io.stalk.static**: 고객이 방문한 웹사이트에 채팅 위켓 또는 채팅 화면을 실행하기 위한 스크립트 입니다. - [https://github.com/xpush/io.stalk.static](https://github.com/xpush/io.stalk.static)

각 서버의 설치 및 실행을 아래에서 확인하시기 바랍니다.
 * [Start XPUSH Chat Server](install_xpush_chat.md)
 * [Start STALK Admin Server](install_stalk_admin.md)
 * [Build Client Chat widget](install_stalk_static.md)

### XPUSH CHAT 서버 설치
github 에서부터 소스를 다운받아 `npm install` 로 필요한 node 모듈을 설치합니다. (현재 최신의 XPUSH-CHAT 서버는 아직 NPM에서 관리하지 않고 있습니다만, 현재 열심히 준비 중입니다.)
``` bash
  $ git clone https://github.com/xpush/xpush-chat.git
  $ cd xpush-chat
  $ npm install
```


<a class="jiver-btn jiver-btn--green" href="https://github.com/smilefam/jiver-sample/tree/master/JiverWebSample/static/libs" target="_blank">Latest JIVER Web SDK - Click here to download</a>

### Sample app
<a class="jiver-btn jiver-btn--green" href="https://github.com/smilefam/jiver-sample" target="_blank">Sample app - Click here to see repository</a>


### JavaScript
`JIVER Web SDK`는 [jQuery](https://jquery.com/)와 [gracefulWebSocket](https://github.com/ffdead/jquery-graceful-websocket)을 필요로 합니다.  
만약, `IE 10`에서 사용하시길 원하는 경우 [Sample](https://github.com/smilefam/jiver-sample/tree/master/JiverWebSample/static/js)에 있는 [gracefulWebSocket](https://github.com/smilefam/jiver-sample/blob/master/JiverWebSample/static/js/jquery.gracefulWebSocket.js)을 다운받아 사용하시길 바랍니다.  

```javascript
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
<script src="jquery.gracefulWebSocket.js"></script>
<script src="libs/jiver-sdk-1.2.1.min.js"></script>
```
