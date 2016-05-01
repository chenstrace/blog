---
title: 使用samba遇到的问题
tags:
  - Samba
categories:
  - Linux使用
date: 2016-04-16 13:35:21
---



<!-- toc -->

### **最终效果**

-   使用Windows作为host，VMware安装Ubuntu作为guest


-   使用VMware Tools的共享文件夹功能在Ubuntu系统中读写Windows系统中的文件


-   使用Samba在Windows中读写Ubuntu系统中的文件



### **遇到的问题**

-   Windows上创建的文件，在Ubuntu中的用户名是``nobody``，用户组是``nogroup``
-   在Ubuntu中创建的文件，Windows上不能写



### **解决方法**

-   在Samba配置中，添加``force user``和``force group``
-   在系统配置中``/etc/login.defs``中修改``umask``为000


### **具体配置**

```shell
[share]
   path = /home/cjl
   browseable = yes 
   writable = yes 
   directory mask = 777 
   create mode = 666 
   security = user
   available = yes 
   public = yes 
   guest ok = yes 
   guest account = cjl 
   force user = cjl 
   force group = cjl 
```



```shell
# Prefix these values with "0" to get octal, "0x" to get hexadecimal.
#
ERASECHAR   0177
KILLCHAR    025 
UMASK       000 
```

