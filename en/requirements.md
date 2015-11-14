Requirements
======================
`STALK`를 설치하여 사용하기 위해서는 nodejs, zookeeper, redis, mongodb가 필요합니다.

`STALK`를 실행하기 위해 필요한 구성요소를 설치하는 방법입니다. 아래는 64bit linux를 기준으로 작성되었으며, 각각 여러분의 환경에 맞게 설치하셔야 합니다. 이미 설치되어 있으면, 이번 장을 건너띄십시오.

### node.js 설치하기
[nodejs installation](http://nodejs.org/download/)를 참조하여 nodejs를 다운로드하고 압축을 해제합니다.
``` bash
$ git clone https://github.com/smilefam/jiver-sample.git
```


### node.js 설치하기
[node.js installation](http://nodejs.org/download/)를 참조하여 nodejs를 다운로드하고 압축을 해제합니다.
``` bash
	$ wget http://nodejs.org/dist/v5.0.0/node-v5.0.0-linux-x64.tar.gz
	$ tar xzvf node-v* && cd node-v*
  $ ./configure
  $ make
  $ sudo make install
```
To check that the installation was successful, you can ask Node to display its version number:
``` bash
  $ node --version
  v5.0.0
```

### zookeeper 설치하고 실행하기.
[zookeeper installation](http://zookeeper.apache.org/doc/trunk/zookeeperStarted.html)를 참조하여 zookeeper를 설치하고 실행합니다. zookeeper 를 실행하기 위해서는 JDK 가 설치되어 있어야 합니다.
아래는 zookeeper 3.4.6을 설치하고 실행하는 코드입니다.
``` bash
	$ wget http://apache.mirror.cdnetworks.com/zookeeper/stable/zookeeper-3.4.6.tar.gz
	$ tar xvf zookeeper-3.4.6.tar.gz
	$ cp zookeeper-3.4.6/conf/zoo_sample.cfg zookeeper-3.4.6/conf/zoo.cfg
	$ cd zookeeper-3.4.6/bin
	$ ./zkServer.sh start
```

### redis 설치하고 실행하기.
[redis installation](http://redis.io/download#installation)를 참조하여 redis를 설치하고 실행합니다.
아래는 redis 3.0.5을 설치하고 실행하는 코드입니다.
``` bash
  $ wget http://download.redis.io/releases/redis-3.0.5.tar.gz
  $ tar xzf redis-3.0.5.tar.gz
  $ cd redis-3.0.5
  $ make
  $ src/redis-server
```

### mongodb 설치하고 실행하기.
[mongodb installation](http://docs.mongodb.org/manual/installation/)를 참조하여 mongodb를 설치하고 실행합니다.
아래는 mongodb 3.0.7을 설치하고 실행하는 코드입니다.
``` bash
	wget --no-check-certificate https://fastdl.mongodb.org/linux/mongodb-linux-x86_64-3.0.7.tgz
	tar xzf mongodb-linux-x86_64-3.0.7.tar.gz
	cd mongodb-linux-x86_64-2.6.4
	mkdir db
	mkdir logs
	bin/mongod --fork --dbpath db --logpath logs
```
   * **Note**: Disk 공간이 3379MB보다 적으면 --smallfiles 옵션을 사용하세요.
``` bash
	bin/mongod --dbpath db --smallfiles
```
