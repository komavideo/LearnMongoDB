文档更新（update）
================

## 知识点

* update(<filter>, <update>, <options>)

### 命令参考网页

https://docs.mongodb.com/manual/reference/method/db.collection.update

## 实战演习

~~~bash
$ mongo
> use komablog;
> db.posts.findOne({"title":"怪物猎人世界评测"});
> db.posts.update({"title":"怪物猎人世界评测"}, {$set: {"rank": 10} });
> db.posts.find();
> db.posts.update({"title":"怪物猎人世界评测"}, {"rank": 99});
> db.posts.find();
> db.posts.update({"tag":"it"}, {$set: {"rank": 50}});
> db.posts.find();
> db.posts.update({"tag":"it"}, {$set: {"rank": 60}}, {multi: true});
> db.posts.find();
~~~

## 课程文件

https://github.com/komavideo/LearnMongoDB

## 小马视频频道

http://komavideo.com
