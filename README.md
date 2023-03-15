# 前端blog（记录我学习前端的过程吧）

[html](#html)<br/>
[css](#css)<br/>


## html
## css
[单行文字溢出省略号表示](#单行文字溢出省略号表示)
### 单行文字溢出省略号表示
```
<!-- 先强制一行内显示 -->
white-space: nowrap;
<!-- 超出部分隐藏 -->
overflow: hidden;
<!-- 超出文字省略号替代 -->
text-overflow: ellipsis;
```

### 多行文本溢出省略号
```
<!-- 因为多文本溢出省略有较大兼容性问题，所以比较适合webKit浏览器或移动端使用 -->
<!-- 依旧先溢出隐藏 -->
overflow: hidden;
<!-- 加省略 -->
text-overflow: ellipsis;
<!-- 弹性伸缩盒子模型显示 -->
display: -webkit-box;
<!-- 限制在一个块元素显示的文本行数（2行） -->
-webkit-line-clamp: 2
<!-- 设置或检索伸缩盒对象的子元素的排列方式 -->
-webkit-box-orient: vertical;
```
基本是cv即用

### margin负值运用
在代码中经常会需要把两个或以上的盒子紧贴一起，但是如果盒子有边框的话会出现边框重合变粗的情况
margin的负值就能解决这个问题

例子：
```
<style>
  ul li {
          float:left;
          list-style:none;
          height:
          weight:
          border: 1px solid black;
          margin-left:-1px;
</style>
```
高亮盒子边框：
```
//主盒子没有加position: relative;的情况下
ul li:hover {
  position: relative;
  border: 1px solid orange;
//如果主盒子加的话
ul li:hover {
  z-index: 1;
  border: 1px solid orange;
```



### 文字围绕浮动元素
两个盒子(被围绕盒子(子盒子)加浮动，文字盒子(父盒子)标准流)

