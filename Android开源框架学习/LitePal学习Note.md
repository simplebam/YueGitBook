# LitePal 学习
* [Android数据库高手秘籍(一)——SQLite命令 - 郭霖的专栏 - CSDN博客](http://blog.csdn.net/guolin_blog/article/details/38461239)
* [LitePal 1.6.0版本来袭，数据加解密功能保障你的应用数据安全](http://mp.weixin.qq.com/s/TSp36cnKLxUmAHjT86UCrQ)


## 番外话
* 这里更多记录 LitePal 一些开发中遇到的问题,由于 LitePal 每次更新都会修复一些bug或者
  把细节做的更好,所以本笔记都会指出 LitePal 版本
* 很多人都问我为什么不用 GreenDao 以及 LiteOrm 甚至 Realm 等数据库,LitePal 在
  Github 上的热度都比不上其他三个,但为什么我还会坚持使用 LitePal 呢?其实这问题真的
  不想说什么,但你用了 litePal 久一点或者说你的关系型数据库学得好的话,我相信无论
  LitePal 还是其他关系型数据库对你来说都是很容易上手的啦


对本笔记有存疑点或者建议的朋友们可Email我:3421448373@qq.com(杨晓)



## LitePal Version_1.6.1 遇到的问题
*  >org.litepal.exceptions.DataSupportException: com.yueyue.testapp.PlanTask needs a default constructor.

   这个问题我查询数据库时候,实体中没有一个默认构造方法/空参构造方法就会遇到这个问题

* >org.litepal.exceptions.DataSupportException: the bind value at index 1 is null

   这问题当我查询或者更新字段为null的时候,比如where("name=?",null) 就会报这个错误
