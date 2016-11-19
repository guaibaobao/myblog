---
title: jQuery
date: 2016-10-02 10:51:36
tags:
---
---
title: jQuery—Ajax
---
一些jQuery跨域请求问题：get,post等几种方式和具体参数

## 总结

### jQuery.post

jQuery.post(url,[data],[callback],[type]) : 使用POST方式来进行异步请求。
	url(String): 发送请求的URL地址。
	data(Map):可选，要发送给服务器的数据，以Keyvalue的键值对形式表示。
	callback（Function）: 可选，载入成功时回调函数（只有当Response的返回状态是success才是调用该方法）。
	type(String):可选， 客户端的请求类型说明如JSON ,XML等等


### jQuery.get

jQuery.get(url,[data],[callback]) 使用GET方式来进行异步请求
	url(String): 发送请求的URL地址
    data(Map): 可选，要发送给服务器的数据，以key/value的键值对形式表示，会作为QueryString附加到请求URL中。
    callback(Function)：可选，载入成功时回调函数（只有当response的返回状态是success才是调用该方法）


### load(url,[data],[callback]) 载入远程的HTML文件代码并插入至DOM中
 	url (String): 请求的HTML页的URL地址。
    data(Map) : 可选参数，发送至服务器的key/value数据。 无参数 get，有参数 post
    callback(Callback): 可选参数 请求完成时(不需要是success)的回调函数。


### jQuery.getScript(url,[callback]) 通过GET方式请求载入并执行一个JavaScript文件



