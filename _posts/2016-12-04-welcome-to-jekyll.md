---
title:  "Jekyll+Github Pages搭建简易博客系列（一）"
categories: 
  - Blog
tags:
  - Blog
---

# --->本地建立Jekyll项目
---

## I. 首先感谢Iulia总结了这个过程并整理成视频，能上YouTube的可以参考一下：

<iframe width="560" height="315" src="https://www.youtube.com/embed/t9qDNe7xk4c" frameborder="0" allowfullscreen></iframe>


## II. 不能上YouTube的可以按照她本人总结文字步骤进行：

### Step_0 使用的工具：
- Win 10 企业版 x64
- Notepad++
- Git Bash

---

### Step_1 准备的软件：
- Ruby 2.0.0及以上版本
- DevKit
- Bundler

---

### Step_2 建立过程：

#### 1）安装Ruby

- [下载地址](https://rubyinstaller.org/downloads/)，下载符合系统的版本；
- 安装时，三个选项全选中；
- 完成后在“此电脑-属性-高级-环境变量”查看是否添加Ruby的环境变量，在git bash中输入“ruby --version”查看版本。

#### 2）安装DevKit

- 下载地址[同上](https://rubyinstaller.org/downloads/)，注意选择和Ruby版本对应的DevKit；
- 解压到目录下，我时放在安装的Ruby目录下，在C盘；
- git bash下cd到Devkit的解压目录，然后执行以下三个命令：
```
ruby dk.rb init
ruby dk.rb review
ruby dk.rb install
```

#### 3）建立本地Jekyll项目

- 从[这里](https://github.com/mmistakes/minimal-mistakes)下载到本地并解压，cd进入到该目录；
- 安装bundler：```gem install bundler```，遇到防火墙提示请同意；
- 安装bundler的依赖：```bundle install```
- 建立本地Jekyll站点：```bundle exec jekyll build```
- 执行本地站点：```bundle exec jekyll serve```，如果执行有问题，用命令```netstat -ano```检查4000端口是否被占用，如果被占用，则记住PID号，在“任务管理器-服务”中停掉

  **如果顺利的话，在浏览器用[http://localhost:4000/](http://localhost:4000/)即可本地访问主页。**

---

### Step_3 修改本地Jekyll站点

- 文章在_posts添加和修改；
- 每次修改后都要重新执行一下```bundle exec jekyll serve```
- 具体博客布局的修改，功能的添加可以参考[这篇文章](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)。

