Install and start XPUSH chat server
======================
Based on the XPUSH` module, `XPUSH-CHAT` with built-in real-time chat function will be responsible for sending and receiving real time messages of` STALK` service.

`XPUSH - CHAT` must be partitioned into Session Server and Channel Server and executed.
 * **Channel Server**: 
As a server that handles the transmission and reception of actual real-time messages, many clients connect to Channel Server and send and receive messages in real time. Channel Server needs to be added and executed as more users are connected.
 * **Session Server**: It is responsible for authenticating the connected user and deciding which server among distributed distributed channel servers to connect to and distributing it.

### 1. XPUSH CHAT Installation
Download the source from github and install the necessary node module for `npm install`.

``` bash
  $ git clone https://github.com/xpush/xpush-chat.git
  $ cd xpush-chat
  $ npm install
```

### 2. Create a configuration file
In order to run `XPUSH - CHAT` server,` XPUSH - CHAT` must use zookeeper, redis, mongodb addresses in the configuration file.
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

### 3. Run Session Server 
``` bash
  $ bin/session-server --config ./config.json --port 8000
```

### 4. Run Channel Server
``` bash
  $ bin/channel-server --config ./config.json --port 9000
```
