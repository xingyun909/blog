---
title: react-native 安装
date: 2017-04-11 12:28:36
tags:
---

网上很多关于react-native 关于mac下或关于Windows下咋开发配置，在Linux下 尤其是ubuntu 14.04 32位下的更少，配置过程中，又有各种坑，还是希望总结一下，希望在学习的小伙伴少走些弯路

关于安装参照[react-native中文网](http://reactnative.cn/docs/0.43/getting-started.html#content)的安装步骤，教程中有些也不必全照着来

###### 安装环境  
  Ubuntu 14.04l LTS  32位

###### 这里列举一些环境配置中的各种坑
所遇到的问题就是一下三大类

  >   
  1 关于npm或node问题
  2 关于Android studio 问题
  3 关于模拟器问题

###### 1 关于npm或node问题
版本问题

  很多问题可能是node或npm所以建议先跟新node和npm，参看[这里](http://www.jianshu.com/p/b32d98c8adb2)


镜像源
关于镜像源设置，参看[这里](https://cnodejs.org/topic/4f9904f9407edba21468f31e)


###### 2 关于Android studio 问题
   * 安卓SDK
   * Java JDK
   * 构建工具gradle   
SDK 和 JDK 在下载和解压好后首先配置PATH，可以再/etc/profile ，或~/.bashrc中 在最后加入

  Jdk path
         export JAVA_HOME=/usr/local/opt/jdk1.8.0_77  //这里路径是jdk解压后所在的路径
         export CLASSPATH=.:$JAVA_HOME/lib:$JAVA_HOME/jre/lib:$CLASSPATH   
         export PATH=$JAVA_HOME/bin:$JAVA_HOME/jre/bin:$PATH  
  SDK path   
           export   ANDROID_HOME = ~/xue/Android/SDK  //这里是安卓SDK所在的路径
           export PATH=$PATH:~/xue/Android/SDK/platform-tools //sdk下面有Android需要工具，所以需要加上
           export PATH=$PATH:~/xue/Android/SDK/tools
##### 注意android sdk 和jdk在Android studio 的设置，  如下图，
![001.png](http://upload-images.jianshu.io/upload_images/1718226-0bf542e4a2e81092.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



![002.png](http://upload-images.jianshu.io/upload_images/1718226-177c3ca87c9c1df7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

构建工具gradle  一般是版本问题 ，可以下载跟新，下载地址，[这里](http://gradle.android-studio.org/)，解压后放入Android studio的gradle目录下，在studio 中设置如下图
![003.png](http://upload-images.jianshu.io/upload_images/1718226-4dd217f74520c97b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#####遇到的错误
 * [Error while Launching activity](https://segmentfault.com/q/1010000005104871/a-1020000005108109)


###### 1 关于模拟器问题  
在Linux 32 下还是不要弄什么虚拟机genymotion了，一是下载不到，二配置还很难说出问题，直接连接手机，参考[这里](http://reactnative.cn/docs/0.43/running-on-device-android.html#content)
注意   
*   小米手机,需要关闭miui优化  参考[这里](http://www.jianshu.com/p/2df69c50bb55)
*   5.0以上的手机
1运行adb reverse tcp:8081 tcp:8081
2不需要更多配置，你就可以使用Reload JS和其它的开发选项了。
*   Android 5.0以需要配置ip ，如下

![
![
![
![
![20160518152047103.png](http://upload-images.jianshu.io/upload_images/1718226-fdd6b30efa001f57.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
](http://upload-images.jianshu.io/upload_images/1718226-ceb88e8ce7554f8d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
](http://upload-images.jianshu.io/upload_images/1718226-47d6fcfc50fd9ac0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
](http://upload-images.jianshu.io/upload_images/1718226-cfe0a6a7261b2227.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
](http://upload-images.jianshu.io/upload_images/1718226-10bf56af9b5878e3.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
