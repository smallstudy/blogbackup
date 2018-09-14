---
layout: post
title: 上传本地文件到github仓库
date: 2018-08-24 20:51:04
tags:
  - github
---
```
git init #初始化本地仓库
git add . #提交本地所有文件到仓库
git commit -m "提交内容" #引号里的是注释内容
git remote add origin git@github.com:youname/youname.git #关联到远程仓库
git pull --rebase origin master #ִ本地文件会有个README.md
git push -u origin master #上传文件
```
`git不能管理空文件，文件夹里必须有文件`
