MongoDB的安装
============

## 知识点

* MongoDB安装文件下载(Windows/Mac)
* Ubuntu Server 16.04 LTS安装(apt)
* mongod服务启动

### MongoDB安装文件下载

https://www.mongodb.com/download-center

### Ubuntu安装

https://docs.mongodb.com/master/tutorial/install-mongodb-on-ubuntu/

~~~bash
$ sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
$ echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.6 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.6.list
$ sudo apt-get update
$ sudo apt-get install -y mongodb-org
$ sudo service mongod start
$ sudo service mongod restart
$ sudo service mongod stop
~~~

### mongod服务启动

~~~bash
$ cd /lib/systemd/system
$ cat mongod.service
$ sudo systemctl start mongod.service
$ sudo systemctl stop mongod.service
$ sudo systemctl enable mongod.service
$ sudo systemctl is-enabled mongod.service
~~~

## 课程文件

https://github.com/komavideo/LearnMongoDB

## 小马视频频道

http://komavideo.com
