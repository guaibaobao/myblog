---
title: CSS3小结
date: 2016-10-26 21:48:02
tags:
---
---
title: css3 弹性盒子模型
---
文章涵盖css3中文字阴影,文字描边,弹性盒子模型,盒模型新增属性,其他的盒模型属性,CSS3分栏布局

## 总结

### 文字阴影

text-shadow：x y blur color


### 文字描边

-webkit-text-stroke:宽度 颜色

### 弹性盒子模型

注意在使用弹性盒模型的时候 父元素必须要加display:flex或
display:inline-box（需要加内核前缀）
box-orient 定义盒模型的布局方向
box-direction 元素排列顺序
box-ordinal-group 设置元素的具体位置


### 盒模型新增属性

box-shadow:[inset] x y blur [spread] color
参数
inset：投影方式
inset：内投影
不给：外投影
x、y：阴影偏移
blur：模糊半径
spread：扩展阴影半径
先扩展原有形状，再开始画阴影
Color

### 其他的盒模型属性

box-reflect 倒影
direction  方向     above|below|left|right;
距离
渐变（可选，后面讲）
resize 自由缩放
Both 水平垂直都可以缩放
Horizontal 只有水平方向可以缩放
Vertical 只有垂直方向可以缩放
注意：一定要配合overflow:auto 一块使用只有水平方向可以缩放
box-sizing 盒模型解析模式
Content-box  标准盒模型 width/height=border+padding+content
Border-box 怪异盒模型 width/height=content
