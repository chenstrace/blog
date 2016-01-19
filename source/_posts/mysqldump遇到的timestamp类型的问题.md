---
title: mysqldump遇到的timestamp类型的问题
tags:
  - mysql
  - mysqldump
categories:
  - 工程实践
date: 2016-01-19 18:01:42
---

#### **现象**

mysqldump导数据到到文件orders.dat，然后用source orders.dat导入。 结果导入后timestamp类型的变量的值从2015-12-21 00:00:00变成了2015-12-21 08:00:00

#### **解决方法**

mysqldump --skip-tz-utc database table_bame --where="date_column BETWEEN '2012-07-01 00:00:00' and '2012-12-01 00:00:00'"
