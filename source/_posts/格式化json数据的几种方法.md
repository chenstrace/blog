---
title: 格式化JSON数据的几种方法
tags:
  - 
categories:
  - 工程实践
date: 2017-10-22 16:29:24
---

- 只有1行JSON数据`read t`，复制粘贴JSON数据，回车，`echo $t|jq`
- 多行JSON数据：`cat<<EOF|jq`，复制粘贴JSON数据，回车，输入EOF，回车
- [https://www.bejson.com](https://www.bejson.com/)
- 使用`Sublime`的`Pretty JSON`插件，快捷键`CTRL+ALT+J`
- 使用`Chrome`的`JSONView`插件

如果没有`jq`，可以使用`python -m json.tool`, 例如：`echo '{"code":0}' |python -m json.tool`

