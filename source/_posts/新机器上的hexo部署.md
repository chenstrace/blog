---
title: 新机器上的hexo部署
categories:
  - Hexo
date: 2017-03-24 11:32:33
---

```
cd ~
npm --registry https://registry.npm.taobao.org info underscore
hexo init xxx
git clone https://github.com/chenstrace/blog.git
cp -r xxx/node_modules blog
cd blog
npm install --save
```

