---
title: node安装配置与使用
date: 2016-06-02 15:25:13
tags:
---

![](images/node.jpg)
# node安装配置与使用
 在安装node网上有甚多的教程，但是安装配置和使用都很分散，以至于我在学习的过程中花费了很多时间，边找资料边实践有时还遇到很多问题，在这里我想把它好好整理整理，希望在学习的同学不用那么麻烦的找。

### node的下载

 
在百度直接搜索nodejs，百度搜索栏的第一个就是，附图
![](images/2.png)
进入node官网，这里有两个版本，一个是稳定版，还有一个是最新版
一般下稳定版就可以了
### node的安装

 这里不多少说，和正常的软件一样，一路下一步直到finish

### 配置

安装完成后，一般要启动node就只有在安装的那个可执行的文件夹里，这里要想在Windows的任何一个盘下运行就需要给它配置一下环境变量，和Java配置差不多直接 “我的电脑”右键“属性”-“高级系统设置”-“高级”-“环境变量”。如下图
![](images/3.jpg)
这里主要是路径和环境变量

编辑path，再里面加入安装node的可执行程序的那个目录，如图
![](images/4.png)
配置然后保存，配置成功，打开cmd，即可以在任意一个地方运行node终端命令行模式

### npm全局路径配置

使用node，就不得不提npm，NPM（node package manager），通常称为node包管理器。顾名思义，它的主要功能就是管理node包，包括：安装、卸载、更新、查看、搜索、发布等。

npm的背后，是基于couchdb的一个数据库，详细记录了每个包的信息，包括作者、版本、依赖、授权信息等。它的一个很重要的作用就是：将开发者从繁琐的包管理工作（版本、依赖等）中解放出来，更加专注于功能的开发

这里主要写一下配置的问题，安装完node，npm就已经自带有了，

```
node -v 
```
就可以查看node当前的版本，这里如果下载和安装npm的工具就会发你全局安装还是本地安装，那些安装的包都会在c盘下，可能都是大家不希望的
我们可以把它放下我们新建的文件夹下node_global，node_cache，如图
![](images/5.png)

	npm config set prefix "D:\node\node_global"<!--配置全局安装目录-->

	npm config set cache "D:\node\node_cache"<!--配置缓存目录-->

配置环境变量path添加    node.exe  的目录文件夹路径 和  D:\Program files\nodejs\node_global （npm设置的全局安装的目录文件夹路径）

配置环境变量NODE_PATH   设置为node_modules的文件夹路径  D:\Program files\nodejs\node_global\node_modules 

	npm config list  <!--查看路径是否配置成功-->

![](images/6.png)

### 设置npm国内镜像

npm由于是国外的，在下载安装其他包肯能装不了，这里要注意了，镜像源可能找不到，
有两种办法，一种是使用国内镜像

	npm config set registry http://registry.npmjs.vitecho.com 

一种是使用淘宝的cnpm，安装一下就行

	npm install -g cnpm --registry=https://registry.npm.taobao.org


##### 以上是我安装过程中总结的几点


   