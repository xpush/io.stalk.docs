Requirements
======================
To use the `STALK` is, nodejs, zookeeper, redis , mongodb is required .

The following is how to install 64bit linux. Please install to suit your environment. If you have already been installed, the xpush installation immediately please.

### node.js
[node.js installation](http://nodejs.org/download/) by referring to Download and unzip the nodejs.
``` bash
	$ wget https://nodejs.org/dist/v6.9.1/node-v6.9.1.tar.gz
	$ tar xzvf node-v* && cd node-v*
	$ ./configure
	$ make
	$ sudo make install
```
Check version
``` bash
	$ node --version
	v6.9.1
```

### Install zookeeper
Install and run zookeeper with reference [zookeeper installation](http://zookeeper.apache.org/doc/trunk/zookeeperStarted.html)

The following is the code to install and run the zookeeper 3.4.9

``` bash
	$ wget http://apache.mirror.cdnetworks.com/zookeeper/stable/zookeeper-3.4.9.tar.gz
	$ tar xvf zookeeper-3.4.9.tar.gz
	$ cp zookeeper-3.4.9/conf/zoo_sample.cfg zookeeper-3.4.9/conf/zoo.cfg
	$ cd zookeeper-3.4.9/bin
	$ ./zkServer.sh start
```

### Install redis
Install and run redis with reference [redis installation](http://redis.io/download#installation)

The follow is the code to install and run redis 3.2.5

``` bash
	$ wget http://download.redis.io/releases/redis-3.2.5.tar.gz
	$ tar xzf redis-3.2.5.tar.gz
	$ cd redis-3.2.5
	$ make
	$ src/redis-server
```

### Install mongodb
Install and run mongodb with reference [mongodb installation](http://docs.mongodb.org/manual/installation/)

The follow is the code to install and run redis 3.4.0

``` bash
	$ wget --no-check-certificate https://www.mongodb.com/dr/fastdl.mongodb.org/linux/mongodb-linux-x86_64-amazon-3.4.0.tgz/download
	$ tar xzf mongodb-linux-x86_64-amazon-3.4.0.tgz
	$ cd mongodb-linux-x86_64-amazon-3.4.0
	$ mkdir db
	$ mkdir logs
	$ bin/mongod --fork --dbpath db --logpath logs
```
   * **Note**: use –smallfiles option if disk space less than 3379MB
``` bash
	$ bin/mongod --dbpath db --smallfiles
```
