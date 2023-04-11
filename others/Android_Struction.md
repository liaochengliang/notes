# Android_Struction

## 一、应用层

应用层包括手机上的所有APP，无论是系统自带的还是用户开发的。他们都是基于第二层应用框架层开发的。

## 二、应用框架层

Android开发人员接触最多的就是框架层，该层提供了各种各样的系统API，开发人员通过使用这些API来构建上一层的各种各样的APP。这些API包括且不限于：Activity Manager(控制Activity的生命周期等)、Notification Manager（提供通知相关的功能）、Content Provider（实现应用程序间的数据共享）、Resource Manager（管理非代码资源，比如布局文件，图片资源，字符资源等等）、View（提供常见的视图控件）、Alarm Manager（提供闹钟相关服务）等等。

## 三、库层

第三层包含两部分内容：

第一部分是Native C\C++系统库层，主要提供一系列第三方类库，常见的有系统C库、多媒体库（播放媒体文件）、SGL（2D图像引擎）、Free Type(渲染位图和矢量字体)、Sqlite（轻量级数据库）、SSL（Secure Socket Layer）、Webkit（提供网络工具）等等；

第二部分是运行环境，包括Dalvik虚拟机和Java核心库。关于Dalvik虚拟机和JVM的区别：Dalvik是基于寄存器的，JVM是基于栈的。JVM运行.class文件，每个.class文件对应一个类；Dalvik虚拟机将.class文件转为.dex文件，只有一个.dex文件，包含了所有的类，并且通过性能优化转为.odex文件。基于寄存器的虚拟机运行速度更快，文件更小，效率更高，适合移动端。另外Dalvik虚拟机需要更多的指令空间。

## 四、内核层

Android系统底层是基于Linux系统的，主要提供各种硬件驱动。