---
title: 我的Hexo博客搭建过程
date: 2016-09-17 23:19:57
tags:
---

# 本地环境
操作系统：Windows 10 (64bit)

# 注册GitHub账号
* 登录https://github.com/，进入“Sign up for GitHub”页面
* 输入username：wuqingtao
* 输入email address：<my email address>
* 输入password：<my password>
* 点击“Sign up for GitHub”，确定注册完成。

# 创建GitHub项目
* 登录https://github.com/，点击右上角“Sign in”进入用户登录页面
* 输入之前注册的<my email address>和<my password>，点击“Sign in”，完成登录
* 点击“Start a project”或者“New repository”，在“Repository name”输入框中输入“wuqingtao.github.io”，check上“Initialize this repository with a README”，点击“Create repository”
* 重复上述操作，创建另一个repository：“my-hexo-blog”
* 至此，完成了两个repository的创建，一个用户发布博客（wuqingtao.github.io），一个用于管理博客代码（my-hexo-blog）

# 安装Git
* 登录https://git-scm.com/download/win
* 点击“64-bit Git for Windows Setup”，下载该安装包
* 确定安装完成

# 安装TortoiseGit
* 登录https://tortoisegit.org/download/
* 点击“Download TortoiseGit 2.2.0 - 64-bit”，下载该安装包
* 确定安装完成

# 安装Node.js
* 登录https://nodejs.org/zh-cn/
* 点击最新的安装包v6.6.0，下载该安装包
* 修改安装目录为“D:\nodejs”
* 确定完成安装

# 进入命令行
* 新建工程目录：E:\prj
* 在该工程目录（E:\prj）下，右键，选择“Git Bash”打开命令行
``` Bash
<allen>@<ALLEN-PC> /E/prj
$
```

# 修改npm镜像源
``` Bash
$ npm config set registry https://registry.npm.taobao.org
```
确定没有错误发生，忽略警告（WARN）

# 安装Hexo
``` Bash
$ npm install hexo-cli -g
```
确定没有错误发生

# 创建hexo博客项目
``` Bash
$ hexo init blog
```

# 安装blog依赖
``` Bash
$ cd blog
$ npm install
```

# 启动本地blog服务
``` Bash
$ hexo server
```
在浏览器中输入“localhost:4000”，如果前面的步骤都正确的化，这个浏览器页面将显示默认的博客页面

# 提交代码到GitHub
* 进入文件管理器目录“E:/prj”
* 邮件点击“Git Clone...”，进入TortoiseGit克隆界面，输入“https://github.com/wuqingtao/my-hexo-blog”，克隆my-hexo-blog至本地目录（E:\prj\my-hexo-blog）
* 拷贝E:\prj\blog下面的所有文件至E:\prj\my-hexo-blog下面
* 删除E:\prj\blog
* 进入E:\prj\my-hexo-blog，邮件点击“Git Commit -> "master"...”，进入TortoiseGit提交界面，全选需要提交的文件，点击“commit”，完成代码提交到本地Git仓库
* 再次右键点击“Git Sync...”，进入TortoiseGit同步界面界面，点击“Push”按钮，完成提交代码到GitHub
至此，代码管理操作完成，后续针对博客的操作，都将在E:\prj\my-hexo-blog中进行

# 修改博客名称
TODO

# 写博文
TODO

# 部署
TODO
