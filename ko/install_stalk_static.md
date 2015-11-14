Install and start XPUSH chat server
======================
`XPUSH` 모듈을 기반으로 실시간 채팅기능을 내장한 `XPUSH-CHAT`는 `STALK`서비스의 실시간 메시지 송수신을 담당하게 됩니다.

`XPUSH-CHAT` 는 Session Server 와 Channel Server 로 구분되어 실행해야 합니다.
 * **Channel Server**: 실제 실시간 메시지 송수신을 처리하는 서버로서, 다수의 Client 가 Channel Server에 접속하여 실시간으로 메시지를 송수신 하게 됩니다. Channel Server 는 접속자가 많아지면 질수록 추가 실행될 필요가 있습니다.
 * **Session Server**: 접속 사용자의 인증을 담당하고, 분산 구성된 다수의 Channel Server 들 중에 어느 서버에 접속해야 하는지 판단하여 분산 할당하는 역할을 담당합니다.

### 1. XPUSH CHAT 소스 다운로드 및 설치
github 에서부터 소스를 다운받아 `npm install` 로 필요한 node 모듈을 설치합니다. (현재 최신의 XPUSH-CHAT 서버는 아직 NPM에서 관리하지 않고 있습니다만, 현재 열심히 준비 중입니다.)
``` bash
  $ git clone https://github.com/xpush/xpush-chat.git
  $ cd xpush-chat
  $ npm install
```

### 2. 설정 파일 작성하기
`XPUSH-CHAT` 서버를 실행하기 위해서는 `XPUSH-CHAT`가 사용할 zookeeper, redis, mongodb 의 주소를 설정파일에 작성해야 합니다.
``` bash
  $ vi config.json
  {
    // Your zookeeper address
    "zookeeper": {"address":"127.0.0.1:2181"},

    // Your redis address
    "redis": {"address":"127.0.0.1:6379"},

    // Your mongo db address
    "mongodb": {"address":"127.0.0.1:27017"}
  }
```  

### 3. Session Server 실행하기.
``` bash
  $ bin/session-server --config ~/config/config.json --port 8000
```

### 4. Channel Server 실행하기.
``` bash
  $ bin/channel-server --config ~/config/config.json --port 9000
```
