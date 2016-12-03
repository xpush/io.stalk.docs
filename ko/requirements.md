Requirements
======================
`STALK`를 설치하여 사용하기 위해서는 nodejs, zookeeper, redis, mongodb가 필요합니다.

`STALK`를 실행하기 위해 필요한 구성요소를 설치하는 방법입니다. 아래는 64bit linux를 기준으로 작성되었으며, 각각 여러분의 환경에 맞게 설치하셔야 합니다. 이미 설치되어 있으면, 이번 장을 건너띄십시오.

### node.js 설치하기
[node.js installation](http://nodejs.org/download/)를 참조하여 nodejs를 다운로드하고 압축을 해제합니다.
``` bash
	$ wget https://nodejs.org/dist/v6.9.1/node-v6.9.1.tar.gz
	$ tar xzvf node-v* && cd node-v*
	$ ./configure
	$ make
	$ sudo make install
```
To check that the installation was successful, you can ask Node to display its version number:
``` bash
	$ node --version
	v6.9.1
```

### zookeeper 설치하고 실행하기.
[zookeeper installation](http://zookeeper.apache.org/doc/trunk/zookeeperStarted.html)를 참조하여 zookeeper를 설치하고 실행합니다. zookeeper 를 실행하기 위해서는 JDK 가 설치되어 있어야 합니다.
아래는 zookeeper 3.4.9을 설치하고 실행하는 코드입니다.
``` bash
	$ wget http://apache.mirror.cdnetworks.com/zookeeper/stable/zookeeper-3.4.9.tar.gz
	$ tar xvf zookeeper-3.4.9.tar.gz
	$ cp zookeeper-3.4.9/conf/zoo_sample.cfg zookeeper-3.4.9/conf/zoo.cfg
	$ cd zookeeper-3.4.9/bin
	$ ./zkServer.sh start
```

### redis 설치하고 실행하기.
[redis installation](http://redis.io/download#installation)를 참조하여 redis를 설치하고 실행합니다.
아래는 redis 3.2.5을 설치하고 실행하는 코드입니다.
``` bash
	$ wget http://download.redis.io/releases/redis-3.2.5.tar.gz
	$ tar xzf redis-3.2.5.tar.gz
	$ cd redis-3.2.5
	$ make
	$ src/redis-server
```

### mongodb 설치하고 실행하기.
[mongodb installation](http://docs.mongodb.org/manual/installation/)를 참조하여 mongodb를 설치하고 실행합니다.
아래는 mongodb 3.4.0을 설치하고 실행하는 코드입니다.
``` bash
	$ wget --no-check-certificate https://www.mongodb.com/dr/fastdl.mongodb.org/linux/mongodb-linux-x86_64-amazon-3.4.0.tgz/download
	$ tar xzf mongodb-linux-x86_64-amazon-3.4.0.tgz
	$ cd mongodb-linux-x86_64-amazon-3.4.0
	$ mkdir db
	$ mkdir logs
	$ bin/mongod --fork --dbpath db --logpath logs
```
   * **Note**: Disk 공간이 3379MB보다 적으면 --smallfiles 옵션을 사용하세요.
``` bash
	$ bin/mongod --dbpath db --smallfiles
```
