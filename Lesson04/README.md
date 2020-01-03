简简单单NoSql
============

## 知识点

* mongo命令行工具
* 建立删除数据库

## 实战演习

~~~bash
$ mongo
> help
> exit
$ mongo
> show dbs;
> use komablog;
> show collections;
> db.createCollection("posts");
> db.createCollection("categories");
> db.createCollection("tags");
> show collections;
> show dbs;
> db.stats();
> db.dropDatabase();
> show dbs;
~~~

## 课程文件

https://github.com/komavideo/LearnMongoDB

## 小马视频频道

http://komavideo.com
