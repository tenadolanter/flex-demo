# flex-layout-demo

## Flex布局简介

Flex英文为flexiable box，翻译为弹性盒子，Flex布局即弹性布局。

Flex布局为盒子模型提供了很大的灵活性，任何一个容器都可以指定为Flex布局，设置方法为：

```bash
.box{
	display: flex;
}
```
行内元素使用Flex布局

```bash
.box{
	display: inline-flex;
}
```
在webkit内核的浏览器上必须加上webkit前缀

```bash
.box{
	display: flex;
	display: -webkit-flex;
}
```

> 注意：使用Flex布局之后，里面的float、clear、vertical-align属性将失效。

## Flex布局中的基本概念

采用 Flex 布局的元素，称为 Flex 容器（flex container），简称"容器"。它的所有子元素自动成为容器成员，称为 Flex 项目（flex item），简称"项目"。

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/case1.jpg)

容器默认存在两根轴：水平的主轴（main axis）和垂直的侧轴（cross axis）。主轴的开始位置（与边框的交叉点）叫做main start，结束位置叫做main end；侧轴的开始位置叫做cross start，结束位置叫做cross end。

项目默认沿主轴排列。单个项目占据的主轴空间叫做main size，占据的侧轴空间叫做cross size。

## 容器的属性

```bash
1、flex-driection
2、flex-wrap
3、flex-flow
4、justify-content
5、align-items
6、align-content
```

> 1、flex-driection设置项目的排列方向，默认为row

```bash
flex-driection: row | row-reverse | column | column-reverse
```
当设置为flex-driection: row，效果：

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/flex-driection1.jpg)

当设置为flex-driection: row-reverse，效果：

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/flex-driection2.jpg)

当设置为flex-driection: column，效果：

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/flex-driection3.jpg)

当设置为flex-driection: column-reverse，效果：

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/flex-driection4.jpg)

如下代码直接复制保存为html文件即可以查看效果：

```bash
<style type="text/css">
.box{
	display: flex;
	display: -webkit-flex;
	/*水平方向，左端对齐*/
	flex-direction: row;
	/*水平方向，右端对齐*/
	/*flex-direction: row-reverse;*/
	/*垂直方向，顶部对齐*/
	/*flex-direction: column;*/
	/*垂直方向，底部对齐*/
	/*flex-direction: column-reverse;*/
	background: #999;
	width: 100%;
}
.box span{
	margin: 10px 10px;
	padding: 10px;
	background: #ff0;
	width: 50px;
}
</style>
<div class="box">
	<span>你好1</span>
	<span>你好2</span>
	<span>你好3</span>
	<span>你好4</span>
</div>
```

> 2、flex-wrap设置项目是否在一条线上，默认为nowrap

```bash
flex-wrap: wrap | nowrap | wrap-reverse
```
当设置为flex-wrap: wrap，效果：

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/flex-wrap1.jpg)

当设置为flex-wrap: nowrap，效果（不换行，默认会缩放）：

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/flex-wrap2.jpg)

当设置为flex-wrap: wrap-reverse，效果：

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/flex-wrap3.jpg)

如下代码直接复制保存为html文件即可以查看效果：

```bash
<style type="text/css">
.box{
	display: flex;
	display: -webkit-flex;
	/*换行*/
	/*flex-wrap: wrap;*/
	/*不换行，默认*/
	/*flex-wrap: nowrap;*/
	/*换行，第一行在下方*/
	/*flex-wrap: wrap-reverse;*/
	background: #999;
	width: 100%;
}
.box span{
	margin: 10px 10px;
	padding: 10px;
	background: #ff0;
	width: 50px;
}
</style>
<div class="box">
	<span>你好1</span>
	<span>你好2</span>
	<span>你好3</span>
	<span>你好4</span>
	<span>你好5</span>
	<span>你好6</span>
	<span>你好7</span>
</div>
```
> 3、flex-flow属性是flex-direction属性和flex-wrap属性的简写形式，默认值为row nowrap

> 4、justify-content属性定义项目在主轴上的对齐方式，默认值为flex-start

```bash
justify-content: flex-start | flex-end | center | space-between | space-around
```
当设置为justify-content: flex-start，效果：

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/justify-content1.jpg)

当设置为justify-content: flex-end，效果：

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/justify-content2.jpg)

当设置为justify-content: center，效果：

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/justify-content3.jpg)

当设置为justify-content: space-between，效果：

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/justify-content4.jpg)

当设置为justify-content: space-around，效果：

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/justify-content5.jpg)

如下代码直接复制保存为html文件即可以查看效果：

```bash
<style type="text/css">
.box{
	display: flex;
	display: -webkit-flex;
	/*默认，项目左对齐*/
	justify-content: flex-start;
	/*项目右对齐*/
	/*justify-content: flex-end;*/
	/*项目居中对齐*/
	/*justify-content: center;*/
	/*项目两端对齐*/
	/*justify-content: space-between;*/
	/*每个项目两侧的间隔相等*/
	/*justify-content: space-around;*/
	background: #999;
	width: 100%;
}
.box span{
	margin: 10px 10px;
	padding: 10px;
	background: #ff0;
	width: 50px;
}
</style>
<div class="box">
	<span>你好1</span>
	<span>你好2</span>
	<span>你好3</span>
	<span>你好4</span>
	<span>你好5</span>
	<span>你好6</span>
	<span>你好7</span>
</div>
```
> 5、align-items属性定义项目在纵轴上的对齐方式，默认值为stretch，适用于项目在纵轴上高度不一样的情况，为了更好的看到效果，我为项目添加了一些样式

```bash
align-items: flex-start | flex-end | center | baseline | stretch
```
当设置为align-items: flex-start，效果：

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/align-items1.jpg)

当设置为align-items: flex-end，效果：

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/align-items2.jpg)

当设置为align-items: center，效果：

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/align-items3.jpg)

当设置为align-items: baseline，效果：

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/align-items4.jpg)

当设置为align-items: stretch，效果：

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/align-items5.jpg)

如下代码直接复制保存为html文件即可以查看效果：

```bash
<style type="text/css">
.box{
	display: flex;
	display: -webkit-flex;
	/*纵轴的顶部对齐*/
	/*align-items: flex-start;*/
	/*纵轴的底部对齐*/
	/*align-items: flex-end;*/
	/*纵轴的中点对齐*/
	/*align-items: center;*/
	/*项目的第一行文字的基线对齐*/
	/*align-items: baseline;*/
	/*默认对齐方式，如果项目未设置高度或设为auto，将占满整个容器的高度*/
	align-items: stretch;
	background: #999;
	width: 100%;
}
.box span{
	margin: 10px 10px;
	padding: 10px;
	background: #ff0;
	width: 50px;
}
.box span:nth-of-type(2n){
	height: 80px;
	padding-top: 20px;
}
</style>
<div class="box">
	<span>你好1</span>
	<span>你好2</span>
	<span>你好3</span>
	<span>你好4</span>
	<span>你好5</span>
	<span>你好6</span>
	<span>你好7</span>
</div>
```




## 项目的属性



## Flex布局使用案例





