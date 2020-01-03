文档的方法
==========

## 知识点

* sort()
* limit()
* skip()

## 实战演习

~~~bash
$ mongo
> use komablog;
> db.posts.find();
> db.posts.find({}, {_id:0}).sort({rank:1});
> db.posts.find({}, {_id:0}).sort({rank:-1});
> db.posts.find({}, {_id:0}).limit(3);
> db.posts.find({}, {_id:0}).sort({rank:-1}).limit(3);
> db.posts.findOne({}, {_id:0});
> db.posts.find({}, {_id:0});
> db.posts.find({}, {_id:0}).limit(3);
> db.posts.find({}, {_id:0}).skip(3).limit(3);
~~~

## 课程文件

https://github.com/komavideo/LearnMongoDB

## 小马视频频道

http://komavideo.com
