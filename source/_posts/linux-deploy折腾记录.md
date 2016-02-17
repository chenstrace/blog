---
title: linux deploy折腾记录
tags:
  - linux deploy 
categories:
  - 工程实践
date: 2016-02-06 15:47:49
---

明天就是春节了，这段时间先后折腾了

-   Godaddy
-   DnsPod
-   Github Pages
-   Gitcafe Pages
-   Hexo (Windows和Mac)
-   XX-Net
-   baidu和google的sitemap
-   MacBook的使用



折腾是能学习到一些东西的，同时也能改进生产效率。

火箭的朋友圈，关于"进取性"和"防御性"工作的论述确实是神似了，一定要去看看那本书了。

说一下最近折腾的`Linux Deploy`吧。很早就知道我的一个哥们折腾过这个东西，然后也知道有一个同类叫做`Complete Linux Installler`。 两个东西的本质相同，关键技术都是`chroot`。

其实那个哥们最早折腾的是`Complete Linux Installer`，而后转向了`Linux Deploy`。后来我问过他`Linux Deploy`的优点，他也跟我讲了，大体是对android版本的兼容更好，更加健壮，上网功能等等。

我手里有两个手机，一个红米1S，一个小米NOTE顶配版。

安装最新的`BusyBox` `Linux Deploy` ，尝试在线和离线的两种安装镜像的方式，都没能成功。

google遇到的问题，搜索到github上面`Linux Deploy`作者的几个回答，包括下载兼容版本的`BusyBox`，改路径之类。没能解决问题。

这期间也尝试装过`Complete Linux Installler`，Ubuntu是安装上了，但是不能ssh，还有动态库的问题。

做过的尝试还有，借了一个Nexus 5的手机，刷小米手机的ROM，都没能成功。而且最新版本的MIUI还把Bootloader给锁了。解锁还要去官方申请，有点恶心。

决定放弃了，但还是不死心。

那个哥们也尝试用最新版本的安装，也失败了。他的折腾经验更丰富一些，告诉我用一下老的版本。

于是选择了`Linux Deploy 1.4.8`这个版本，在线安装的方式，安装了一个ubuntu的版本，具体叫什么忘记了，启动时提示，`sshd`失败。

死马当活马医吧，看到可选的版本里面还有一个叫Trusty的，我只知道trust这个单词，呵呵，信他一回吧，又尝试在线安装了这个版本，结果还真成功了。真的有一定的运气成分了。

然后用电脑ssh上来了，tcpdump抓了一下包。以后调试APP的问题，不用fiddler了。

年后等MIUI官方把Bootloader锁解开，再在小米NOTE上安装一个。


