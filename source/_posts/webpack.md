---
title: webpack
date: 2016-11-05 23:43:26
tags:
---
---
title: webpack的搭建
---

  大半夜洗了个头，估计一时半会儿还睡不了觉。突然想到以后可能要用到webpack，今天就回顾一下webpack的搭建，方便自己以后用起来顺手些。
  主要步骤为：

> * 1.引入webpack依赖，全局安装webpack
> * 2.

------

>## 一、引入webpack依赖

### **1.1安装全局webpack**
在一个盘符中创建一个工程，（注意不要放在中文目录，以免不必要的麻烦）然后打开CMD，输入以下命令。

`npm install webpack -g`

### ***1.2创建配置文件***
在项目工程的根目录创建三个或多个webpack配置文件
（1）web.base.config.js  //公用的配置放在这里面
（2）web.develop.config.js  //开发环境中用到的配置文件
（3）web.publish.config.js   //生产环境中用到的配置文件


#### ***1.2.1在develop中配置基本内容***
```
var path = require('path');

module.exports = {
    entry:path.resolve(__dirname,'src/js/app.js'),//文件入口
    output: {                                     //输出文件配置信息
        path: path.resolve(__dirname, 'deploy/js'),
        filename: 'bundle.js',
    }
}
```
备注：这里说明一下，这里用到的时一种模块化的规范conmmonjs,想一行代码是导入，第三行是导出。
#### ***1.2.2运行检错***
 法一：在根目录运行webpack的命令，默认会去查找名称为webpack.config.js的文件执行，如果没有就会报配置信息没有配置的错误。。
 法二：还可以通过运行下面的命令进行要执行的配置文件的选择
webpack –-config  webpack.develop.config.js

。。。未完待续。。。（好吧，我承认我困得睁不开眼了，，睡觉去~）