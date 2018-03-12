# Android 面经基础篇


## 番外话
* 本教程是基于[《Android第一行代码》](./Android第一行代码/Android第一行代码Note.md)的目录而制作的


## 第2章 先从看的到的入手-探究Activity
* [1.1、Activity的生命周期 - CSDN博客]( http://blog.csdn.net/lonelyroamer/article/details/8927940)
* [深入理解Activity的生命周期 - 简书]( https://www.jianshu.com/p/fb44584daee3)
* [Android中Activity数据的保存和恢复 - 简书]( https://www.jianshu.com/p/6622434511f7)
* [Android-Activity所应该了解的大概就这样。（上） - 简书 ](https://www.jianshu.com/p/33d0a0abd990)

### 笔记补充
* 在开启新的Activity时候,前一个Activity先Pause，后一个Activity的构造方法才走
* 如果你的应用程序中没有生命任何有个活动作为主活动,这程序依然可以正常安装的,只是你无法在启动器中看到或者阿凯这个应用程序.这种程序一般都是作为第三方服务提供给其他应用在内部进行调用的,如支付宝快捷支付服务
