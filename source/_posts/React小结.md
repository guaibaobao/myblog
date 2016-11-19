---
title: React小结
date: 2016-10-15 23:12:01
tags:
---
# React
谈谈自己对React的浅了解，大致阅读了一些关于React的文章，来总结点笔记留给以后的自己。
  - React是facebook开源的一个用于构建用户界面的javascript库，应用时总从UI出发
  - 顺应了web开发组件化的趋势
  - 专注于MVC架构中的V视图。（React会自动处理所有用户页面更新）

节点小热身:
  - React是为了解决：构建随着时间数据不断变化的大规模应用程序。
  - 为什么要用虚拟DOM？
  
    答：因为在用js操作DOM的过程中效率非常低（Js对虚拟DOM操作是对DOM进行操作和之    前的虚拟DOM对象进行比较形成新的虚拟DOM）

React的[安装] 和 [语法] 

### 1.在之前安装的Webpack的基础上，在原来文件中打开命令窗口

输入指令npm install  --save-dev   react;

  npm install --save-dev  react-dom

### 2.在publish文件下：创建一个index.html并编辑其内容为：

```sh
  <script  type="text/javascript" src="node-module/dist/react.min.js"></scrpt>
          <script  type="text/javascript" src="node-module/dist/react-dom.min.js"></scrpt>
          <script  type="text/javascript" src="https://unpkg.com/babel-core@5.8.38/browser.min.js"></scrpt>（这个网址是在线解析的引用）
           <script  type="text/babel">
                   ReactDOM.render(
                              <div>Hello World</div>,
                              document.getElementById("demo")
                    ); 
           </scrpt>
     说明：render中的第一个参数是：组件名，第二个参数是：DOM容器。        

```

创建组件时：

```sh
<script  type="text/babel">
                         class Hello extends React.Component{
                                   render( ){
                                             return <div>Hello World</div>;
                                   }
                         }
               ReactDOM.render(
                         <Hello/>,//自闭合标签
                         document.getElementById("demo")
               );
          </script>

```

jsx的语法规则：
```sh
  在src目录下的js文件下的component文件下创建World.jsx文件并编辑为：
    import React from "react";
     import ReactDOM from "react-dom";
     export default class Hello extends React.Component{
    render(){
            return <div>World</div>
    }
}
在app.js中写入：
import React from "react";
import ReactDOM from "react-dom";
import Hello from './src/js/component/World.jsx'
ReactDOM.render(
        <Hello/>,
        document.getElementById("dukewei")
    )
   最后在命令窗口输入：npm run develop   
```
组件的生命周期（状态回调）：
```sh
在component目录下建个YaPing文件夹再其下建YaPing.jsx并写入：
                                       import React from 'react';
let initValue = '幸运女生。。。';
export default class YaPing extends React.Component{
    getInitDefaultProps(){
            console.log("123123");
    }
    getInitState(){
            console.log("456456");
    }
    componentWillMount() {
        console.log('即将开始美丽的童话。。。');
    }
    componentDidMount() {
        console.log('童话世界里的公主。。。');  
    }
    shouldComponentUpdate(nextProps,nextState){
        initValue:"童话里都是骗人的。。。";
        console.log("你不可能是我的王子！！！");
        return true;
    }
    myClick = () =>{
        this.setState({happy:"meet you..."});
        console.log('遇见最美的你');
    }

    render(){
        return <p><span onClick={this.myClick}>{initValue}</span></p>
    }

};
编辑app.js:

                                                  import React from "react";
import ReactDOM from "react-dom";
import YaPing from './src/js/component/YaPing/YaPing.jsx';
ReactDOM.render(
        <div><YaPing/></div>,
        document.getElementById("dukewei")
);
最后在命令窗口输入：npm run develop
```
```sh
以上纯属个人见解,仅供参考。。。
```

