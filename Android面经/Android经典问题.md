# Android经典问题


## 借鉴博客
* [一个三非渣本的安卓秋招之路 | 温斯渤 | To Be A Better Man. ](http://wensibo.top/2017/10/29/interview/#%E6%9C%80%E8%BD%BB%E6%9D%BE%E5%B9%BD%E9%BB%98%E7%9A%84%E9%9D%A2%E8%AF%95%E2%80%94%E2%80%94%E2%80%94%E2%80%94%E7%8F%8D%E7%88%B1%E7%BD%91)


### 经典问题
* 介绍一下RecyclerView的原理以及优点
  * [RecyclerView 的三种LayoutManager - 简书 ](https://www.jianshu.com/p/6d278427b18b)
  * [深入浅出 RecyclerView|开源实验室-张涛 ](https://kymjs.com/code/2016/07/10/01/)
* 为什么会选用Material Design？
  * 在 Material Design 还没有出来之前,Android 标准的界面设计风格并不是特别被
    大众所接受,很多公司都觉得最近完全可以设计出更加好看的界面,从而导致 Android
    平台的界面风格长期难于得到统一.
  * PS:5.0之前的系统 UI 等很丑,但 5.0之后的系统 UI 都对用户很友好,看起来很舒服
* Android 5.0之后的版本和之前的版本有什么区别？
  * [Android各个版本的区别 - CSDN博客 ](https://blog.csdn.net/u012758803/article/details/54844903)
  * 可以参看《android进阶之光》的第一章：
    * 全新的 Material Design 设计风格
    * 支持多种设备，比如智能设计、平板电脑、笔记本电脑、智能电视、汽车以及智能手表
    * 全新的通知中心设计
    * 支持64 位 ART 虚拟机，抛弃了之前一直使用的 Dalvik 虚拟机
    * OverView
    * 设备识别解锁
    * OK Google 语音指令
* DVM与ART的区别？
  * [Android内存优化（一）DVM和ART原理初探 - CSDN博客 ](https://blog.csdn.net/itachi85/article/details/72861179)
* Custom-Tabs-Client是什么？
  * [提升体验-支持Chrome Custom Tabs - 泡在网上的日子 ](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2017/0106/6945.html)
* MVP与MVC有什么区别？
  * [MVC，MVP 和 MVVM 的图示 - 阮一峰的网络日志 ](http://www.ruanyifeng.com/blog/2015/02/mvcmvp_mvvm.html)
* Handler机制？Looper原理？
  * [Android异步消息处理机制完全解析，带你从源码的角度彻底理解 - CSDN博客](https://blog.csdn.net/guolin_blog/article/details/9991569)
  * [Android中Thread、Handler、Looper、MessageQueue的原理分析 - CSDN博客](https://blog.csdn.net/bboyfeiyu/article/details/38555547)
  * [Android消息机制，你真的了解Handler吗？ - 郭霖 | 十条 ](http://www.10tiao.com/html/227/201711/2650241824/1.html)
  * [Android 消息机制——你真的了解Handler？ - CSDN博客 ](https://blog.csdn.net/qian520ao/article/details/78262289#7-%E5%A6%82%E4%BD%95%E5%A4%84%E7%90%86handler-%E4%BD%BF%E7%94%A8%E4%B8%8D%E5%BD%93%E5%AF%BC%E8%87%B4%E7%9A%84%E5%86%85%E5%AD%98%E6%B3%84%E9%9C%B2)
  * 在dispatchMessage里面
    * 第一个msg.callback指的callback接口是Message.obtain(handler,callback)
      ;这里的callback其实就是一个Runnable类型
    * mCallback是构造方法Handler(looper,callback,async)传进来;这里的callback
      是一个接口，里面有handleMessage方法
    * 最后一个handleMessage(msg)才是我们熟悉的handler创建时候需要重写的方法
    (这个方法本身为空实现，需要我们自己重写)。
    * tips：
      * Handler post()方法传入的runnable之后属于msg.callback
      * View post()方法调用的是 Handler post()方法
      * Activity runOnUiThread()方法如果当前线程是主线程，直接调用run方法；
        否则调用的是Handler post()方法
* Activity的启动流程？(AIDL问题)
  * [Android Binder之应用层精彩解析 - 郭霖 | 十条 ](http://www.10tiao.com/html/227/201711/2650241725/1.html)
  * [Android Launcher启动Activity的工作过程 - 郭霖 | 十条 ](http://www.10tiao.com/html/227/201711/2650241786/1.html)
* HandlerThread实现原理
  * [Android HandlerThread 总结使用 - 赵彦军 - 博客园 ](https://www.cnblogs.com/zhaoyanjun/p/6062880.html)
* ActivityThread的main方法主要做了哪些操作？
  * [ActivityThread的main方法究竟做了什么？ - CSDN博客 ](https://blog.csdn.net/melodev/article/details/51959347)
* 什么情况下使用单例模式？
  * [Android设计模式之单例模式 - stormzhang ](http://stormzhang.com/designpattern/2016/03/27/android-design-pattern-singleton/)
  * [你真的会写单例吗 | Blankj's Blog ](https://blankj.com/2016/04/21/really-use-singleton/)
  * 应用场景:
    * 控制资源的使用，通过线程同步来控制资源的并发访问；
    * 控制实例产生的数量，达到节约资源的目的。
    * 作为通信媒介使用，也就是数据共享，它可以在不建立直接关联的条件下，让多个不
      相关的两个线程或者进程之间实现通信。
* volatile域
  * [Java并发编程（三）volatile域 - CSDN博客 ](https://blog.csdn.net/itachi85/article/details/50274169)
* 了解过哪些设计模式？分别详细说一下优缺点？
  * [simplebam/JavaDesignPatterns: Java常用的设计模式](https://github.com/simplebam/JavaDesignPatterns)
* 说一下网络连接的状态码的含义？
  * [网络：HTTP协议状态码详解-hiyachen-ChinaUnix博客 ](http://m.blog.chinaunix.net/uid-7374279-id-4844638.html)
* GET和POST两种基本请求方法的区别
  * [GET和POST两种基本请求方法的区别 - 在途中# - 博客园 ](http://www.cnblogs.com/logsharing/p/8448446.html)
* Java NIO和IO的主要区别
  * [Java NIO和IO的主要区别 - THISISPAN - 博客园 ](http://www.cnblogs.com/panxuejun/p/8631423.html)
* 说一下长连接的优点和缺点？
  * [HTTP长连接和短连接 - WhyWin - 博客园 ](http://www.cnblogs.com/0201zcr/p/4694945.html)
* 为什么静态内部类不会造成内存泄漏？
  * [Android 非静态内部类/匿名类引起的内存泄漏 - CSDN博客 ](https://blog.csdn.net/u010618194/article/details/64147538)
* java多线程的三个特性？原理分别是什么？
  * [多线程编程中三个特性 - CSDN博客 ](https://blog.csdn.net/xiong_hui_hui/article/details/51241338)
