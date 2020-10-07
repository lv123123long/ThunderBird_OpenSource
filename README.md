源码释放说明：

1、源码释放的目的是让所有人清楚地看到在雷鸟下载中，引发360等安全软件告警的是哪些操作，其后的源码是什么样的，以解除大家的困扰。
   你们可以看到，编译后的exe在单独执行时（非VS开发环境下），360会对其警告提示，甚至偶尔极端情况下，直接提示木马病毒，要求清除掉，
   但其实后台代码啥都没做！这就是所谓的安全软件干的勾当！

2、界面设计用到了 DSkin界面库，各位在没有开发库授权的情况下，无法直接打开窗体设计器进行查看（否则会自动退出VS环境），所以直接查看代码，即可。

3、你可以对源码进行修改、编译、运行，其目的是验证（证明）雷鸟源码的安全性，并不意味着授权你基于此框架，进行二次开发，或借助雷鸟之名，发布软件。

4、出于保护软件未来持续可用的考虑，下载功能实现部分的源码未做放出，相信大家可以理解，除非您是想让雷鸟 “从开源，到窒息”，o(╯□╰)o 。


官网地址：http://www.thunderbird.bar   
下载地址：https://www.lanzoux.com/b01bdspaj


重要说明：此Github站点，不作任何交流与答疑工作，有任何问题，请访问在线网址——http://www.thunderbird.bar


==========

再补充详细点：

1、为什么要求管理员权限运行？

原因：一，确保能顺利读写软件自身的配置文件。避免在非管理用户状态下，软件下载后被无意中置于一些要求管理员权限才能读写的路径，导致配置文件更新失败；二，读取系统中不同文件类型注册的默认图标，使得云盘浏览时文件图标显示正确。

2、软件运行过程中，为何会默认关掉网络分析相关的应用？

原因：确保下载算法不被针对。

3、为何在点击登录时，会显示警告“有程序正在进行可疑操作,建议阻止。......程序正在进行远程线程注入...”？

原因：在软件官网 https://www.kancloud.cn/myzfb/thunderbird/1761695 ，已经说得很清楚，这是因为登录功能，软件开发用到了浏览器组件，作为非360白名单中的浏览器软件联网访问网页时，都会有这样的警告，且访问HTTPS网址时，还会弹出“有程序正在修改受信证书发行者”警告，这一点疑问，自己下载雷鸟开源代码，看看编译结果运行时是不是会出现上述两个警告，再看看源码里啥操作都没有，自会明白。


