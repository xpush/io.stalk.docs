Install and start STALK Admin Server
======================
`STALK Admin Server` is administrtion site that manage real-time interaction system with the customer. It provide features such as statistics and management.

### 1. STALK Admin Server Installation
``` bash
  $ git clone https://github.com/xpush/io.stalk.admin.git
  $ cd io.stalk.admin
  $ bower install
  $ npm install
```

### 2. Configration
To run `STALK Admin Server`, you need to set the Session server address and the application name of `XPUSH-CHAT`
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

### 3. STALK Admin Server Execute
``` bash
  $ grunt serve --config ./config.js
```
