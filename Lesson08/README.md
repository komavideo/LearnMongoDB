复杂条件抽文档
=============

## 知识点

* db.[collection_name].find({"":"", "":""})
* db.[collection_name].find({$or:[{...},{...}]});
* db.[collection_name].find({"": {$in: [...]}});
* db.[collection_name].find({"": {$exists: true}});

## 实战演习

~~~bash
$ mongo
> use komablog;
> db.posts.find();
> db.posts.find({"title": /u/, "rank":{$gte:5} });
> db.posts.find({$or: [{"title": /u/}, {"rank":{$gte:4}}] });
> db.posts.find({"rank": {$in: [3,4]} });
> db.posts.insert({ "title":"惊！骑士发生重大交易", "istop": true });
> db.posts.find({"istop": {$exists: true} });
~~~

## 课程文件

https://github.com/komavideo/LearnMongoDB

## 小马视频频道

http://komavideo.com
