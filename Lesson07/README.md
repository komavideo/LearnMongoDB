带条件的文档
===========

## 知识点

* db.[collection_name].find({"":""})
* $gte, $gt, $lte, $lt
* $eq, $ne
* 正则表达式:/k/, /^k/
* db.[collection_name].distinct("field_name");

## 实战演习

~~~bash
$ mongo
> use komablog;
> db.posts.remove({});
> db.posts.insert({title:"怪物猎人世界评测","rank":2,"tag":"game"});
> db.posts.insert({title:"纸片马里奥试玩体验","rank":1,"tag":"game"});
> db.posts.insert({title:"Utunbu16LTS的安装","rank":3,"tag":"it"});
> db.posts.insert({title:"信长之野望大志销量突破10000","rank":4,"tag":"game"});
> db.posts.insert({title:"Ruby的开发效率真的很高吗","rank":7,"tag":"it"});
> db.posts.insert({title:"塞尔达传说最近出了DLC","rank":4,"tag":"game"});
> db.posts.find({"tag": "game"});
> db.posts.find({"rank": {$gte: 4}});
> db.posts.find({"rank": {$gt: 4}});
> db.posts.find({"rank": {$lte: 4}});
> db.posts.find({"rank": {$lt: 4}});
> db.posts.find({"title": /u/});
> db.posts.find({"title": /^R/});
> db.posts.find({"title": /^U/});
> db.posts.distinct("tag");
~~~

## 课程文件

https://github.com/komavideo/LearnMongoDB

## 小马视频频道

http://komavideo.com
