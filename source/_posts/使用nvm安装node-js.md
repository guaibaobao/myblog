---
title: 使用nvm安装node.js
date: 2016-10-23 18:35:42
tags:
---
# 使用nvm安装node.js

------

经过了一次一次的打击我也是心里充满了压力，可是压力并没有改变什么所以我要写点有用的。。。

> * 首先要解压nvm.rar包
> * 使用管理员权限运行install.cmd在命令窗口中输入当前文件夹的地址
> * 修改生成的setting.txt（root：D：\Develop\nvm--当前文件夹路径  path: D:\Develop\nodejs--配置后面要生成的目录   arch: 64--机器位   proxy: none）
> * 配置nvm的环境变量，让其能够在cmd中使用其变量
    （1）点计算机右键选属性
    （2）点高级系统设置再选环境变量
    （3）在用户变量表中选新建再设置变量名（NVM_HOME）和变量值（D：\develop\nvm）
    （4）在path的变量值后面添加%NVM_HOME%;
    （5）最后在计算机搜索框中输入%NVM_HOME%检验是否安装成功
> * 使用nvm命令生成nodejs(文件夹）快捷方式
    （1）点计算机右键选属性
    （2）点高级系统设置再选环境变量
    （3）在用户变量表中选新建再设置变量名（NVM_SYMLINK）和变量值（D：\develop\nvm）
    （4）在path的变量值后面添加%NVM_SYMLINK%;
    （5）最后在计算机搜索框中输入%NVM_SYMLINK%检验是否安装成功
> *配置npm所有工具集的环境变量
    （1）在path的变量值后面添加%NPM_HOME%;
    （2）最后在计算机搜索框中输入%NPM_HOME%检验是否安装成功
> *.改变npm的安装路径
    （1）打开命令窗口，在窗口中输入echo “”.npmrc
    （2）在C盘中点击（用户文件夹），再点击内部的Administrator查看是否创建。npmrc文件夹
    （3）用记事本的方式打开.npmrc文件夹,并编辑其内容为：
            cache=D:\Develop\nvm\npm-cache（安装时的缓存）
            prefix=D:\Develop\nvm\npm（将工具安装到哪）
> *进行最后一步
    （1）以上步骤完成之后，在命令窗口输入http_server回车，然后把npm中的http_server删除
    （2）然后在命令窗口中输入npm install -g http-server回车下载http-server
> *注意：npm下载安装工具（安装包的管理工具）；
         windows的环境变量添加到PATH，新增一个变量，是变量添加

        这只是我个人的一点总结，希望以后会有用。




