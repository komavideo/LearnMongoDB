操作文档（Document）
===================

## 知识点

* MongoDB数据文档的操作

## 实战演习

~~~bash
$ mongo
> use komablog;
> show collections;
> db.createCollection("posts");
> db.posts.insert(
... {
...     title: "我的第一篇博客",
...     content: "已经开始写博客了，太激动了。"
... }
... );
> show collections;
> db.posts.find();
> db.posts.insert(
... {
...     title: "我的第二篇博客",
...     content: "写点什么好呢？",
...     tag: ["未分类"]
... }
... );
> db.posts.find();
> for(var i = 3; i <=10; i++ ) {
...     db.posts.insert({
...         title: "我的第" + i + "篇博客"
...     });
... }
> db.posts.find();
> db.posts.count();
> db.posts.remove({});
> db.posts.count();
> db.posts.find();
~~~

## 课程文件

https://github.com/komavideo/LearnMongoDB

## 小马视频频道

http://komavideo.com
