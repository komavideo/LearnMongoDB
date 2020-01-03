备份和恢复
==========

## 知识点

* mongodump
* mongorestore

## 实战演习

~~~bash
$ mongo
> show dbs;
> use komablog;
> db.posts.find({}, {_id:0});
> exit
$ mkdir dbbak
$ cd dbbak
$ mongodump -d komablog
$ ls
$ mongo komablog
> db.posts.find({}, {_id:0});
> db.posts.remove({});
> db.posts.find({}, {_id:0});
> exit
$ mongorestore --drop
$ mongo komablog
> db.posts.find({}, {_id:0});
> exit
$ mongodump --help
~~~

## 课程文件

https://github.com/komavideo/LearnMongoDB

## 小马视频频道

http://komavideo.com
