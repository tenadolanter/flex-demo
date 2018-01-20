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

容器默认存在两根轴：水平的主轴（main axis）和垂直的交叉轴（cross axis）。主轴的开始位置（与边框的交叉点）叫做main start，结束位置叫做main end；侧轴的开始位置叫做cross start，结束位置叫做cross end。

项目默认沿主轴排列。单个项目占据的主轴空间叫做main size，占据的侧轴空间叫做cross size。

## 容器的属性

```bash
flex-driection
flex-wrap
flex-flow
justify-content
align-items
align-content
```

> flex-driection设置项目的排列方向

```bash
flex-driection: row | row-reverse | column | column-reverse
```

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/flex-driection1.jpg)

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/flex-driection2.jpg)

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/flex-driection3.jpg)

![Alt text](https://raw.githubusercontent.com/tenadolanter/flex-layout-demo/master/images/flex-driection4.jpg)

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



## 项目的属性



## Flex布局使用案例





