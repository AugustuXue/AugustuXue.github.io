---
title: OutLook微软邮件设置——添加QQ邮箱及Gmail邮箱
date: 2021-03-03 11:34:15
tags: 
  - 教程
  - 分享
---

# OutLook微软邮件设置——添加QQ邮箱及Gmail邮箱

## 添加QQ邮箱

QQ邮箱一般是我们经常使用的一种邮箱了，手机还好，但PC端每次收邮件的时候总要专门登录QQ，打开QQ邮箱，而微软有自己的邮件应用OutLook，却总是添加不进去，昨晚找了些参考，总算成功

* 1、打开mail.qq.com，登录自己的账号

* 2、点击左上角的“设置”图标

  ![屏幕截图 2021-03-03 103322](https://gitee.com/augustusxue/augustu_image/raw/master/img/20210303103822.png)

* 3、向下滚动，来到“**POP3/IMAP/SMTP/Exchange/CardDAV/CalDAV服务**”

* 4、开启IMAP服务（不是POP3）

  ![屏幕截图 2021-03-03 104139](https://gitee.com/augustusxue/augustu_image/raw/master/img/20210303104240.png)

  IMAP与POP3区别：![IMAP及POP3有什么区别?](http://nos.netease.com/help/588fcc36fc540643d84c80addabb00ec.jpg)

* 5、点击黄色提示框内的“生成授权码”，按提示发送信息后点击“我已发送”获取授权码，复制备用

  ![屏幕截图 2021-03-03 104548](https://gitee.com/augustusxue/augustu_image/raw/master/img/20210303104557.png)

* 6、打开OutLook,添加账户，选择其他账户，电子邮件地址填写QQ邮箱即可，名称没有具体要求，密码填写刚刚取得的授权码

  <img src="https://gitee.com/augustusxue/augustu_image/raw/master/img/20210303104728.png" alt="image-20210303104727994" style="zoom: 67%;" />

* 7、点击登录，完成

## 添加Gmail邮箱

Gmail有多方便使用过的同学应该不用我多说吧，但它想要日常使用还是差了点意思，想要把它添加进OutLook，PC端上就算是挂代理也奈何不了UWP应用，当然你上软路由当我没说,uwp不能被代理原因如下

> Win10 所有 UWP 应用均运行在被称为 App Container 的虚拟沙箱环境中，App Container 可以保证应用安全性，但同时也阻止了网络流量发送到本机（即 loopback）， 使大部分网络抓包调试工具无法对 UWP 应用进行流量分析。同样的，该机制也阻止了 UWP 应用访问 localhost，即使你在系统设置中启用了代理，也无法令 UWP 应用访问本地代理服务器。



### 方法一 缺点：可能有延迟 优点：无需代理

* 1、登录Gmail邮箱，右上角点击“设置”——一个齿轮样式的图标

* 2、点击“查看所有设置”

* 3、点击“转发和POP/IMAP”

  ![](https://gitee.com/augustusxue/augustu_image/raw/master/img/20210303111050.png)

* 4、“IMAP访问”处点击“启用IMAP”

* 5、登录Google账号，点击“安全性”

  ![image-20210303110619527](https://gitee.com/augustusxue/augustu_image/raw/master/img/20210303110619.png)

* 6、

  * #### 启用了两步验证的账户

    选择“登录google”，进入“应用专用密码”子栏

    [![img](https://gitee.com/augustusxue/augustu_image/raw/master/img/20210303111415.jpeg)](https://pdf-lib.org/Images/UpLoadImages/2020112172149620.jpg)

    [![img](https://gitee.com/augustusxue/augustu_image/raw/master/img/20210303111412.jpeg)](https://pdf-lib.org/Images/UpLoadImages/2020112172159683.jpg)

    按实际情况选择设备和应用，生成应用专用密码并复制， 在要连接到 Gmail 帐户（或添加 Gmail 帐户）的应用中，可将此密码与 Gmail 地址一起使用。这一组合将对使用 Gmail 帐户的应用授予该帐户的完全访问权限。

    [![img](https://gitee.com/augustusxue/augustu_image/raw/master/img/20210303111407.jpeg)](https://pdf-lib.org/Images/UpLoadImages/2020112172231870.jpg)

    [![img](https://gitee.com/augustusxue/augustu_image/raw/master/img/20210303111402.jpeg)](https://pdf-lib.org/Images/UpLoadImages/2020112172240370.jpg)

  * #### 未启用两步验证的账户

    选择“登录与安全”中的“关联的应用和网站”， 将“允许安全性更低的应用”设置为“开” ，然后关闭窗口

    [![img](https://gitee.com/augustusxue/augustu_image/raw/master/img/20210303111509.jpeg)](https://pdf-lib.org/Images/UpLoadImages/2020112172035495.jpg)

    [![img](https://gitee.com/augustusxue/augustu_image/raw/master/img/20210303111512.jpeg)](https://pdf-lib.org/Images/UpLoadImages/2020112172043230.jpg)

* 7、向win10邮件app添加gmail账户

  打开win10邮件中的添加账户，选择添加的类型为高级设置而不是google，并进入“Internet电子邮件”

  [![img](https://pdf-lib.org/Images/UpLoadImages/2020112172322574.jpg)](https://pdf-lib.org/Images/UpLoadImages/2020112172322574.jpg)

  账户设置填写内容按下图所示进行填写即可，需要特别提示的是密码栏：若未开启两步认证请输入gmail密码；若已开启两步认证请输入准备工作中复制的应用专用密码！登录后即可使用gmail并进行同步了。

  [![img](https://gitee.com/augustusxue/augustu_image/raw/master/img/20210303111644.jpeg)](https://pdf-lib.org/Images/UpLoadImages/202011217252411.jpg)

### 方法二 （推荐）

#### 1、如果代理使用Clash

* 在General页面点击UWP Loopback 旁边的EnableLookback.exe或者Launch Helper

* 在弹出的窗口里选择“microsoft.windows.authhost.…”（看不完全的可以最大化后在“DisplayName”一栏里拉长）
* 点击“save change”
* 开启系统接管
* 直接添加Google邮箱

#### 2、代理使用其他类型

* 下载[Fiddler](https://www.telerik.com/fiddler)
* 点击左上角的【WinConfig】
* 剩下步骤同上

*添加Gmail邮箱方法一中有部分存在引用，如有侵权，请联系我*





