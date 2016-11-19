---
title: GIT与GitHub以及博客的创建
date: 2016-10-12 12:38:30
tags:
---

# GIT与GitHub以及博客的创建


**GIT**代码管理工具，可将自己本地的代码上传到 GitHub远程仓库中进行保管，个人觉得还是很好用的，毕竟以前的代码管理有点low。



#### 一、github远程仓库提交

- .建一个项目，在项目中打开命令窗口，输入git init对git进行初始化
- .在项目中添加文件夹（如：css  js 并在文件夹中添加内容main.css  main.js,）输入git status查看git的状态，查看文件夹是否添加，如果没有添加，输入git add . 进行添加
- 在命令窗口输入git commit -m "任意内容 "（这是进行日志提交）
- 将本地文件上传到远程仓库中（自己创建的githhub的仓库）在窗口中输入git remote add origin +github仓库的地址
- 在窗口中输入remote -v
- 在窗口中输入git push -u origin master（将本地文件推送到远程仓库中）

#### 二.创建忽略清单文件
- 在窗口中输入（echo " " >.gitignore）(在本地项目中会自动生成gitignore文件，并在。gitignore）
- 输入git status查看git的状态
- 如果没有则添加输入git add

#### 三.将代码回归到（由哈希值决定）
- 在.git文件中多次修改代码，并多次提交（git commit -m" 日志说明"，不同的修改内容有不同的日志说明）
- 提交后输入 git log窗口中会显示多次提交的哈希值（哈希值是commit后面的代码）
- 在窗口输入git reset --hard +（哈希值）.git中的代码会由哈希值决定

#### 四.克隆远程仓库的代码到本地
- 在本地文件中打开命令窗口输入git clone +（远程仓库的地址）

#### 五. git分支
- 创建新分支：
- 在命令窗口输入 git branch 查看仓库分支
- 输入 git branch gh-pages 新建分支名
- git branch 查看现在的仓库分支
- git checkout gh-pages 跳转至新建分支（switched to branch 'gh-pages'）
- git push -u origin gh-pages 提交至新建分支
（在仓库目录下的settings中可点击网址访问提交页面）

#### 六. hexo 工具
- 新建文件夹右键打开命令窗口   使用npm 安装hexo      输入 npm install -g hexo    
- 初始化 hexo     hexo init blog    会自动生成一个blog
- 点击blog进入  打开命令窗口在命令窗口输入 hexo generate  生成静态页面  （出现一个public）
- 修改   _config.yml   文件  （
				deploy:
                type: git
                repository:(用空格键开)网址
                branch: gh-pages
）
- 在命令窗口输入  hexo server 启动本地服务进行测试。
- 在blog下打开命令窗口输入 npm install hexo-deployer-git --save下载安装hexo-deployer-git
- 在命令窗口输入  hexo deploy --generate  发布到github.



