文档的特殊更新
=============

## 知识点

* upsert:有则更新，无则追加
* remove:条件删除数据

## 实战演习

~~~bash
$ mongo
> use komablog;
> db.posts.find({}, {_id:0});
> db.posts.update({title:"其实创造比大志好玩"}, {title:"其实创造比大志好玩", "rank":5,"tag":"game"});
> db.posts.find({}, {_id:0});
> db.posts.update({title:"其实创造比大志好玩"}, {title:"其实创造比大志好玩", "rank":5,"tag":"game"}, {upsert:true});
> db.posts.find({}, {_id:0});
> db.posts.update({title:"其实创造比大志好玩"}, {title:"其实创造比大志好玩", "rank":7,"tag":"game"}, {upsert:true});
> db.posts.find({}, {_id:0});
> db.posts.remove({title:"其实创造比大志好玩"});
> db.posts.find({}, {_id:0});
~~~

## 课程文件

https://github.com/komavideo/LearnMongoDB

## 小马视频频道

http://komavideo.com
