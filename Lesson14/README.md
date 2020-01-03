使用索引
========

## 知识点

* getIndexes()
* createIndex({...}, {...})
* dropIndex({...})

## 实战演习

~~~bash
$ mongo
> use komablog;
> db.posts.getIndexes();
> db.posts.createIndex({rank:-1});
> db.posts.getIndexes();
> db.posts.dropIndex({rank:-1});
> db.posts.getIndexes();
> db.posts.createIndex({title:1}, {unique:true});
> db.posts.getIndexes();
> db.posts.find({}, {_id:0});
> db.posts.insert({title:"怪物猎人世界评测"});
~~~

## 课程文件

https://github.com/komavideo/LearnMongoDB

## 小马视频频道

http://komavideo.com
