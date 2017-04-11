---
title: markdown笔记
date: 2016-03-13 21:25:02
tags:
	--工具
---
![](markdown.jpg)
![](images/markdown.jpg)
## 一 Markdown是什么？

Markdown 是一种用来写作的轻量级「标记语言」，它用简洁的语法代替排版，而不像一般我们用的字处理软件 Word 或 Pages 有大量的排版、字体设置。它使我们专心于码字，用「标记」语法，来代替常见的排版格式。例如此文从内容到格式，甚至插图，键盘就可以通通搞定了。目前来看，支持 Markdown 语法的编辑器有很多，包括很多网站（例如简书）也支持了 Markdown 的文字录入 

## 二 Markdown有哪些功能？

* 方便的`导入导出`功能
    *  直接把一个markdown的文本文件拖放到当前这个页面就可以了
    *  导出为一个html格式的文件，样式一点也不会丢失
* 编辑和预览`同步滚动`，所见即所得（右上角设置）
* `VIM快捷键`支持，方便vim党们快速的操作 （右上角设置）
* 强大的`自定义CSS`功能，方便定制自己的展示
* 有数量也有质量的`主题`,编辑器和预览区域
* 完美兼容`Github`的markdown语法
* 预览区域`代码高亮`
* 所有选项自动记忆

## 三 Markdown的语法
### 标题
***
# h1
## h2
### h3
#### h4
##### h5
###### h6
***

### 区块元素

一个 Markdown 段落是由一个或多个连续的文本行组成，
它的前后要有一个以上的空行（空行的定义是显示上看起来像是空的，
便会被视为空行。比方说，若某一行只包含空格和制表符，则该行也会被视为空行）。
普通段落不该用空格或制表符来缩进


若要换行，在插入处先按入两个以上的空格然后回车


### 区块引用 Blockquotes
***
> 这是引用
>> 这是引用
>>> 这是引用 嵌套


### 列表
***
##### 水果

* 苹果
* 香蕉
* 梨子


1.  苹果
1.  香蕉
1.  梨子


### 分隔线

```c
***    表示分割线 
* * *   表示分割线 
*****   表示分割线 

```
***
* * *
*****


### 链接


This is [http://baidu.com](http://baidu.com/ "Title") inline link.

this link[ http://baidu.com](http://baidu.com/) has no title attribute

转为html如下

    <p>This is <a href="http://http://baidu.com/" title="Title">
    an example</a> inline link.</p>
    
    <p><a href="http://example.net/">This link</a> has no
    title attribute.</p>


这是百度连接 [百度] [1]
这是腾讯链接[腾讯] [2]
这是阿里巴巴链接 [阿里巴巴] [3].

  [1]: http://www.baidu.com/     "百度"
  [2]: http://www.qq.com/        "腾讯"
  [3]: http://www.alibaba.com/   "阿里"

### 强调
效果如下：
***

*single asterisks*

_single underscores_

**double asterisks**

__double underscores__

转化为

        <em>single asterisks</em>
        
        <em>single underscores</em>
        
        <strong>double asterisks</strong>
        
        <strong>double underscores</strong>



### 代码

效果如下：
***
Use the `printf()` function.

    写法：  Use the `printf()` function.
    
    转化为
    <p>Use the <code>printf()</code> function.</p>

    
    
### 图片插入


*    一个惊叹号 !
*   接着一个方括号，里面放上图片的替代文字
*    接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上 选择性的 'title' 文字。



![Alt text](/path/to/img.jpg)

    写法： ![Alt text](/path/to/img.jpg)
    
    转化为
    <p>Use the <code>printf()</code> function.</p>

### JavaScript代码
效果如下
```JavaScript
  var ihubo = {
    nickName  : "草依山",
    site : "http://jser.me"
  }
```
写法
    ```JavaScript
      var ihubo = {
        nickName  : "草依山",
        site : "http://jser.me"
      }
    ```
    

***

#### 以上是markdown的一些基本用法








