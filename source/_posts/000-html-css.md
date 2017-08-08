---
title: 000_html_css
date: 2016-04-08 12:03:07
tags:
---

##  HTML CSS  

``` bash
###★技巧★ 取消鼠标移动选中文本的
user-select:none


###★技巧★ display:inline-block   
display:inline-block  
和 
line-height 联合使用

###★技巧★  屏幕出现多余的地方，空出来，左右跑，滑动
position: flex;  同时在一个div里时，会出问题
position: relative;


####★技巧★   布局：  计算器布局
flex:1;  把屏幕分三分之一
flex:2;  分三分之二

####★技巧★   文字下划线
<u>Search</u>

####★技巧★   平移
当给choice1 或 choice2 添加 active 时，让choice3左右移动
.xuanze .choice1.active~ .choice3{
  transform:translate3d(0rem,0,0);
}
.xuanze .choice2.active~ .choice3{
  transform:translate3d(1.5rem,0,0);
}


#####    overflow:scroll  滚动有问题
使用用原生滚动条

####★技巧★  nobr   强制不换行
<nobr>强制不换行</nobr>

####★技巧★   百分号
width:percentage( $i / $num );
0.32--> 32%

####★技巧★
ul>li{$}*5

<ul>
    <li>1</li>
    <li>2</li>
    <li>3</li>
    <li>4</li>
    <li>5</li>
</ul>


####★技巧★
position: absolute;
z-index: 15;

####★技巧★ 移动端 头部，底部固定
html和body 用  宽高100% 定，overflow:scroll；
top 和 bottom用display:absolute;

overflow-x: scroll;
x轴滚动


####★技巧★  图片精灵
background: url("../img/gs_geshou_03.png") 50%/cover;

background: url("../img/gs_geshou_03.png") 50%/cover;
    /*background: url("../img/gs_geshou_03.png");*/
    /*background-size: contain;*/

background-size: cover;				/*  不变形 等比缩放  覆盖充满全屏*/
background-size: 300px;				/*  */
background-size: contain;			/*  不变形 仅一张图片放满屏*/

★技巧★
图片,优先考虑直接放图片还是background-image:url("")

####★技巧★
flex：1  是简写

用flex之后，
	浮动  
	text-align  
	vertical-align   垂直对齐
会失效

display: -webkit-flex;
display: flex;
display: inline-flex;  //行内元素

align-content:stretch   默认占满整个容器。但高度不设置或设置为auto的时候。


####★技巧★   flex-flow:
	/* flex-flow: <'flex-direction'> */
flex-flow: row;
flex-flow: row-reverse;
flex-flow: column;
flex-flow: column-reverse;

	/* flex-flow: <'flex-wrap'> */
flex-flow: nowrap;
flex-flow: wrap;
flex-flow: wrap-reverse;

	/* flex-flow: <'flex-direction'> and <'flex-wrap'> */
flex-flow: row nowrap;
flex-flow: column wrap;
flex-flow: column-reverse wrap-reverse;


####★技巧★
<input type="search" class="kuang" placeholder=" 红米4X  小米电视4A 49寸" ><br>
placeholder
搜索框内输入字儿时" 红米4X  小米电视4A 49寸" 会消失

####★技巧★
<!--逻辑像素-->
    <!--逻辑像素-->
    <!--实际像素-->
    <!--视口 一般手机浏览器的viewpoort = 980px -->
    <!--  把手机浏览器的viewpoort改成手机的逻辑像素 -->

 <!--   视口  手机的视口  不加 <meat>的时候像素是980px
                             加<meat>
    视口  手机里的浏览器 默认展示的大小-->


####★技巧★    /* 固定宽度 */
	.container{
		margin: 0 auto;
	}

####★技巧★    a链接后面加一句    target='_blank'  就会在新的页面打开
<a href="apple/index.html" target='_blank'>苹果页面</a>

####★技巧★    设置字体
font-family: "苹方";

####★技巧★   li 撑不开 ul  数学运算符
height:calc(100% - 50px);

####★技巧★   li 撑不开 ul

子元素撑不开父元素
因为子元素浮动
解决方法：清除子元素的浮动

####★技巧★   margin 同时写4个
padding: 20px 30px 20px 10px;     上、右、下、左。顺时针顺序写
margin  一样同时写4个

####★技巧★   雨点
filter: blur(2px);

####★技巧★
section   部分 章节
nav

####★技巧★   鼠标移入手势
CSS中加入：
cursor: pointer;

####★技巧★	 选择非 `<p>` 元素的每个元素。
:not(selector)    
	:not(p)



<!-- <!-- <!-- 目录 --> --> -->

出错点

技巧

笔记


/* /* /* /* /* 0320 */ */ */ */ */
HTML

标签

字体效果标签
颜色
水平线
特殊符号
a 链接 
CSS样式
伪类选择器 

/* /* /* /* /* 0321 */ */ */ */ */

块元素    行内元素    行内块元素

盒模型

padding

margin

文档流

/*清除默认样式*/

hover



/* /* /* /* /* 0322 */ */ */ */ */

.background{}

图片精灵技术

水平线设置

form表单：




/* /* /* /* /* 0323 */ */ */ */ */

form表单：

控件 

按钮  输入框 复选框

定位 position:




/* /* /* /* /* 0324 */ */ */ */ */

table	表格  属性：

tr

td

th		标题；默认加粗，居中




/* /* /* /* /* 0327 */ */ */ */ */

iframe:		内联子窗口

<style>		文本样式：

iconfont    添加文字图标

column		用户界面

resize		拖拽

box-sizing	改变盒子模型

outline		轮廓（不占位置）

border-radius	倒圆角

box-shadow		阴影

border-image 	引入边框图片

background:linear-gradient    渐变

倒影


透明度  透明色	  opacity	鼠标移动过去1秒显示

过渡	transition

旋转	transform




视频连接：

2D特效

transform





/* /* /* /* /* 0328 */ */ */ */ */

3D特效：

perspective		场景

定义动画规则	animation-name:

@keyframes animation1


CSS选择器：
 /* /* CSS1 */ */ 

 /* /* CSS2 */ */ 

 /* /* CSS3 */ */ 


active	鼠标点击效果





/* /* /* /* /* 0329 */ */ */ */ */

响应式：

@media screen and (max-width: 800px)

两端对齐	text-align: justify;

苹果


/* /* /* /* /* 0330 */ */ */ */ */

十二栅格化



/* /* /* /* /*　规范　 */ */ */ */ */








































<!-- <!-- <!-- 出错点 --> --> -->

◆出错点◆
动画和2D\3D特效不一样!
animation-iteration-count: infinite;
/* 动画 无限播放次数 */
animation-duration: 1s;
/* 必须 动画时间 */
animation-timing-function: linear;


◆出错点◆
字体也用rem
font-size: 0.12rem;


◆出错点◆
margin:0 auto;时不能 float:left;


◆出错点◆
设置浮动考虑父元素是否设置宽高


◆出错点◆
一个大块不设高度，用里面的小块撑，多个小块没有设高度时，大块只是第一个块儿撑起来，需要给大块设置 overflow:hidden;


◆出错点◆
加 position: absolute 会使 margin：0 auto 失效，无法居中


◆出错点◆
1.下拉框无法覆盖下拉框下边的东西，有可能是没设置背景色。


◆出错点◆
2.缩小看一下哪一块被挤了，用 overflow:hidden;  把超出部分隐藏。



◆出错点◆
缩小出现进度条
可能是padding值或box-sizing: border-box;


◆出错点◆
去掉下进度条
box-sizing: border-box;


◆出错点◆
清除默认样式
*{
	margin: 0;
	padding: 0;
	list-style: none;
	font-size: 12px;
}

img{
	display: block;
}

a{
	text-decoration: none;
}




















★技巧★

◇技巧◇

◆技巧◆
pink    cyan   purple


{/* /* /* /* /* 技巧 */ */ */ */ */




★技巧★
★技巧★
★技巧★
★技巧★
★技巧★
★技巧★
★技巧★
<meta name="viewport" content="width=device-width,user-scalable=no">
    <!-- 将布局视口==视觉视口 -->




★技巧★
标签：dl dt dd article section form nav header footer button 


★技巧★
	物理像素    750*1334

	逻辑像素    375*667

	布局视口    980

	视觉视口    375
	
	理想视口



★技巧★
计算移动端页面布局

height:calc(100%-3rem);

main{
		width: 100%;
		/* height: calc(100% - 0.88rem - 0.88rem); */
		position: absolute;
		top: 0.88rem;
		bottom: 0.88rem;
		background: blue;
	}




★技巧★{
层级--优先级：

	 定位+float
	 定位：
	 position：static

	 浮动：让块元素无间隙的在一行内排列
	 div不浮动时，margin上下共同的部分，谁的大用谁的


★技巧★
居中
position: absolute;
top:50%;
margin-top: -35px;



★技巧★
右对齐
text-align:right;


★技巧★
:not()
否定伪类选择器
选择除某个元素以外的所有元素.
 
 
 
★技巧★
段落文字行间距
调line-height 0~0.5



★技巧★
解决移动端屏幕滚动时,上边的栏和下边栏闪屏方法.
}html,body{
	width: 100%;
	height: 100%;
	overflow: hidden;
}
body{
	overflow: scroll;
}
/*上边栏*/
.shangbianlan{
	position: absolute;
	top: 0;
	left: 0;
}
/*下边栏*/
.xiabianlan{
	position: absolute;
	bottom: 0;
	left: 0;
}




★技巧★
倒三角
.box{
	width: 0;
	height: 0;
	border-left:1px solid rgba(0,0,0,0) ;
	border-left:1px solid blue ;
	border-left:1px solid rgba(0,0,0,0) ;
	
}



★技巧★
英语单词拆开写   
photos  写到这一行满了，剩下的地方到下一行
拆开的地方-





★技巧★
直接在文字后边加   <br> 可换行
<li style="color: #2DC0FD;font-size: 0.36rem;" >互联网公司的命脉在于产品 <br></li>


★技巧★
十二栅格化/二十栅格化不用设内宽了(1200px)


★技巧★
图片精灵
图片只设置宽或设置高,否则图片会变形


★技巧★
去除input的边框属性
outline: none;
border-style: none;


★技巧★
ul>li{  }*10  --> TAB
div.key{$$}*19  序列





★技巧★{
浏览器内核  	SU  引擎搜索

内核		浏览器				前缀
Tvident 	IE  			-ms- 
Gecko 		火狐 			-moz- 
webkit 		谷歌 			-webkit-




}
★技巧★{	
<!--长方形-->
<svg>
	<rect width="" height=" " style="fill:rgb(0,0,255)">
</svg>




}★技巧★{
h1~h6 	有默认样式   文字、标题
p标签   无样式		 段落



}★技巧★{
span 标签
display:line-block;
		block;



}★技巧★{
/*第五个之后所有的div*/
.box>div:nth-child(5)~div{
	margin-top: 10px;
}


}★技巧★{
banner图在导航栏下边时，先设置导航图，放在1级大块里，banner图和导航栏并列为2级小块。

{


}★技巧★{
sublime    
 查看--》缩进--》缩进格数




★技巧★  
直接给元素类 添加 style="color:#C40000;" 
<div class="a1" style="color:#C40000;">
<a href="" style="color:red;">针织衫</a>


★技巧★   
三角形
border-top: 3px solid rgba(0, 0, 0, 1.0);
border-left: 3px solid rgba(0, 0, 0,0);
border-right: 3px solid rgba(0, 0, 0,0); 


★技巧★
font-family: "微软雅黑","苹方";


★技巧★
html 页面顺序
<body>
    <header>
    <!-- 头部 -->
    <nav>
    <!-- 菜单导航、链接导航 -->
    <article>
    <!-- 主体内容 -->
    <footer>
    <!-- 页面的底部（页脚） -->
</body>



★技巧★
在div命名中添加 style="color:red"  样式改变属性。
<div style="color:red" class="box1 col-xs-4 col-sm-12 col-md-4 col-lg-4">

<style>包含样式。相当于CSS属性设置的地方</style>

<script>脚本语言</script>


★技巧★
box-sizing: border-box;
    去掉下进度条


★技巧★
清除默认样式
*{
	margin: 0;
	padding: 0;
	list-style: none;
	font-size: 12px;
}
img{
	display: block;
}
a{
	text-decoration: none;
}


★技巧★
3./* /* /* 定义盒子 */ */ 注意浮动 */
.box{
	width:1200px ;
	height: 500px;
	margin:0 auto ;
	/* background: red; */
	/* border: 2px solid #000;
	/* padding-left: 100px; */
	/* padding-right:  100px; */
	}

	/* /* /* 定义块 */ */ */
	/* 左边一整块 */
	.box .son:nth-child(1){
		width: 50%;
		height: 100%;
		float: left;
		background: blue;
	}
	/* 右上一块 */
	.box .son:nth-child(2){
		width: 50%;
		height: 50%;
		float: left;
		background: red;
	}
	/* 右下的二分之一左边块 */
	.box .son:nth-child(3){
		width: 25%;
		height: 50%;
		float: left;
		background: green;
	}
	/* 右下的二分之一右边块 */
	.box .son:nth-child(4){
		width: 25%;
		height: 50%;
		float: left;
		background: purple;
	}



是只选择header下的这个i，i下的其他内容，其他i不选。
.header>i{



★技巧★
1.提取网页图片：
	右键--审查元素--找到图片的链接--选中--拖到新窗口--保存
	右键--审查元素--application--top--img-图片--保存

★技巧★
2.分隔栏间的竖线可以用div的右边框设置成黑色

★技巧★
水平线设置：
<hr style=" height:2px;border:none;border-top:2px dotted #185598;" />
height:2px;是hr的高度
border:none;是没有边框
border-top:2px dotted #185598;是设置横线的样式
dotted  虚线  #185598  颜色



★技巧★
1.	outline: none;  去掉边框的鼠标效果
	border: none;   去掉边框

2.  left: 0;
    top: 0;
    right: 0;
    bottom: 0;
    margin: auto;
    /*  上下左右居中 */

    top: 0;
    bottom: 0;
    margin: auto;
    /* 垂直居中 */

3.  border-radius: ;
    /* 圆角属性 数值是12px  50% */

4.  /* 层级 */ 必须在定位上做层级优先
    position: fixed;
    z-index: 10; 


★技巧★
5.<!-- 下拉 -->
利用display：block；
.box .son{
	width: 404px;
	height: 412px;
	margin: 0 auto;
	margin-top: 60px;
	display: none;
}
.box:hover .son{
	display: block;
}




★技巧★{
<!-- 行内标签  进度条-->
html技能：
进度条：<meter min="0" max="10" value="6"></meter>
<time></time>
进程条：<progress> </progress>




★技巧★
.box:before,.box:after{
	content: "";
}
/* 伪类选择器下必须加 content: ""; */


★技巧★{
-webkit-text-fill-color: ;:  red;    
/* 查看兼容性  在冒号前按table键  can i use*/






★技巧★
/* 浮动  */
transform: translateY(-10px);
transform: translateY(-50%);
        /* 浮动 Y轴   平移他自己的50%*/


★技巧★
进度条
html技能<meter min="0" max="10" value="6"></meter>
<br>

★技巧★
调用iconfont
<i class="iconfont gouwuchekong"> </i>


★技巧★
transition: all 2s ease;
监测放在.box{本体}本体中时，鼠标移物会动，移走以后会变化

放在.box：hover{}中时，鼠标移物会动，移走以后不会变化


★技巧★
灭点、透视点：立体图形各条边的延伸线所产生的相交点


★技巧★
定位：
position: absolute;
left right:  一起时优先left;
top bottom:   一起时优先top


★技巧★
浮动停止条件：    float: 
	1.遇到父元素
	2.遇到拥有浮动样式的兄弟元素


清除浮动的三种方式：  qingchu
1.clear: both;
2.clear:left;
3
.box:after,.box:before{
	content: "";
	display: block;
	clear: both;
}

	.row{  // 对父元素清除浮动
	    // 父元素 : 不清除浮动父元素为高度0，清除浮动后为200px
	    position: relative;
	    width:100%;
	    &::after{            //清除浮动
	        content: '';
	        clear: both;
	        display: block;
	    }
	}



★技巧★
2.高度自动
height:auto;



★技巧★
a标签需要单独对它进行属性设置才能变

★技巧★
.nav .con1{
	padding: 0 20px;
	box-sizing: border-box;
	/* 盒子加padding后边框超出屏幕，加box-sizing来改变模型，使其占满框 */
	}

★技巧★
6.CSS :after 选择器
在每个 <p> 元素的内容之后插入新内容：



★技巧★
在响应式设计中，不给div重新设计的话有可能会继承最原始的参数。
解决方法：清除默认样式
margin-bottom: 1px;
margin-top: 1px;
margin-right: 0;
margin-left: 0;


★技巧★
元素可见不可见
h1.visible {visibility:visible}
h1.invisible {visibility:visible}




★网站★
1.网站模板 http://www.templatesy.com/

can i use  

lantera		蓝灯翻墙
youtube		
github		注册账号

花瓣
500px
摄图网









































































/* /* /* /* /* 0320 */ */ */ */ */
{
	html 承载内容
	CSS承载样式
	JS承载效果
html 超文本标记语言
HyperText Markup Language
标签：是最重要的 。以尖括号开始，以尖括号结束。中间小写英文单词。   
	  通常情况下，标签是成对出现的.带“/”是结束标签
	  标签可以嵌套标签
CSS	层叠样式表
Cascading Style Sheets

选择器    我们想要定义一个样式规则，作用于页面中的某些元素那		么我们把这条样式规则就称为选择器

路径：  绝对路径<!--从根目录C盘开始寻找一直找到当前位置-->
		相对路径<!--对本身去寻找。即直接在本文件的同级当中寻找-->

alt="图片"   错误提示

	<em>跳转</em>
 
10.标签： 	 
/*id选择器     优先级100*/		#box{}
/*类名选择器   优先级10*/		.box{}
/*标签选择器   优先级1*/		box{}
/*通用选择器   优先级0*/		*{}    星号
/*群组选择器          */		ul,li{} 
整个页面中的标签都会选中。通用选择器，比如定义整个页面中的字体 */ 

/*后代选择器*/		.box div{  /*单独对下边box的div进行设置，及选择所有的后代*/  }
      				只选择它的后代

/*子类选择器*/		.box>.key{}   选择孙子辈的 

11.顺序：<head> <style></style> <body>
在<style>  中写子类选择器的属性  </style>
<body>	中写元素  </body>


*{
	font-size:  ;
	list-style:none;	/*清楚默认样式*/
}


8.知识点：

height：				设置高
weight：  				设置宽
margin： 0 auto :  		让块元素居中
text-line:				水平居中、对齐方式
background:				设置背景颜色
color：					设置颜色
font-size:				设置字体大小
font-weight：bold   	设置粗体
float:left:				向左浮动

border-width:2px;
border-style:solid;		/* solid 直线    dotted 点线    dashed 虚线*/
border-color:red;		/* red	 #000	rgb(0,0,0) 0~255	rgba(0,0,0,1/0); a:透明度 */

border 0px solid #000;  			设置边框和颜色
border 0px solid red;  				设置边框和颜色
border-bottom: 2px solid red;						设置边框和颜色   直线
border-left: 2px dotted rgb(0, 255, 0);				设置边框和颜色   点线
border-right: 2px dashed rgba(0, 0, 255, 1.0);*/	设置边框和颜色   虚线   a:透明度


div.key{$$}*19  ---->   <div class="key">01</div>			序列
						<div class="key key2">01</div>		设置类名标签属性

<div class="key key5">
    <img src="img/jian.png" alt="图片" width="35px" height="25px">  </div>
在文字中插入图片。再在css中 .key5{}  进行属性设置，对图片进行调整位置。


10.标签： 	 及顺序：<head> <style> <body>
/*id选择器     优先级100*/		#box{}
/*类名选择器   优先级10*/		.box{}
/*标签选择器   优先级1*/		box{}
/*星号选择器   优先级0*/		*{} 

/*后代选择器*/		.box div{  /*单独对下边box的div进行设置，及选择所有的后代*/  }
      				只选择它的后代

/*子类选择器*/		.box>.key{}   选择孙子辈的 

在<style>  中写子类选择器的属性  </style>
<body>	中写元素  </body>


1.绿色的 是属性名=属性值
1.写html、CSS程序最基本分3个文件，CSS文件夹、img文件夹、index.html,其中CSS文件夹中有index.css文件。
2.html为超文本语言，它最重要的是标签。它以尖括号开始，尖括号结束，中间小写英文单词，通常情况下，标签是成对出现的，带“/”结束。标签可以嵌套使用。
3.CSS 是层叠样式表   包含---->index.html
4.img文件中包含说需要展示的文件
5.每天写一个“笔记.txt”文件，用于记录当天的笔记。
6.在index.html中写程序。  !+TAB就会出来程序文本内容，可直接在它上面写。
7.注释：<!--   -->
9.在index.css文件中写标签属性。
 整个页面中的标签都会选中。通用选择器，比如定义整个页面中的字体 */  
11.绿色的  是属性名=属性值
12可以用截屏软件对字体、图片进行测量，测量宽、高，以像素为单位，可以提取其颜色进行设置
13.程序：
<!DOCTYPE html>			 <!--声明-->
<html lang="en"> 	 	<!--主体 根部 语言格式 --> 
<head>  				<!--头部-->	  
	<meta charset="UTF-8">    	<!--字符标码格式-->
	<title>标题</title>   		<!--标题的名字 -->
	<link rel="stylesheet" href="CSS/index.css">		<!-- link 链接 rel 属性名=“属性值”  href 地址 路径-->

    <img src="img/2017-03-20_102041.png"  alt="" width="200px" height="200px">  
	<!-- img 链接   src 地址 路径  alt 报错名=“报错显示”  -->

	<a href="index1.html">跳转    是a标签。
	
	
	
///////////字体效果标签///////////
<h1>...</h1> //标题字（最大）
<h6>...</h6> //标题字（最小）
<b>	...</b>  //粗体字
<strong>...</strong> //粗体字（强调）
<i>...</i>   //斜体字
<em>...</em> //斜体字（强调）
<u>...</u>   底线
<strike>...</strike> //删除线
<s>...</s>   //删除线（缩写）
<del>...</del> //删除线（表示删除）


///////////颜色///////////
aqua  black  blue   fuchsia
gray  green  lime   maroon
navy  olive  purple red
silver teal  white  yellow



//////////水平线////////////

 <hr/>水平线
 <hr size=“9”>水平线(设定大小)
 <hr width=“80%”>水平线(设定宽度)
 <hr color=“ff0000”>水平线(设定颜色)
 <br/>(换行)
 <p>...</p> (段落)



//////////特殊符号////////////

代码 效果 代码 效果
&quot; “ &amp; &
&lt; < &gt; >
&nbsp; 空格 &copy; ©
&sect; § &curren; ¤

///////// a 链接 /////////////

<a href=“地址” target=“” title=“”></a>
– target2个值：
• _blank 在新窗口中打开链接
• _self 在当前窗体打开链接,此为默认值


////////// CSS样式 ////////////
 行内样式表 > 其他的样式表
 其他的样式表，优先级一样，按照导入的顺序来确定他们是否起作用。

行内样式
<div style=“属性1:值1;属性2:值2;”></div>

嵌入样式
<style type=“text/css”>
选择器{属性1:值1;属性2:值2;}
</style>

外部样式
<link rel=“stylesheet” type=“text/css”
href=“url”>

导入样式
@import url(外部样式表位置)；


///////////  伪类选择器   ///////////
a:link {color: #FF0000} /* 未访问的链接 */
 a:visited {color: #00FF00} /* 已访问的链接 */
 a:hover {color: #FF00FF} /* 鼠标移动到链接上*/
 a:active {color: #0000FF} /* 选定的链接 */

p:first-letter{ font-size: 2em; font-variant: small-caps;}
 它可以选中段落p中的第一个字母或中文字符。
 p:first-line { font-size: 2em; float: left;}
 用于选中元素中的首行文本。
//////////////////////






//////////////////////

/*
<!DOCTYPE html>			 <!--声明-->
<html lang="en"> 	<!--主体 根部 语言格式 --> 
<head>  				<!--头部-->	  
	<meta charset="UTF-8">    <!--字符标码格式-->
	<title>标题</title>   <!--标题的名字 -->
	<link rel="stylesheet" href="CSS/index.css">		<!-- link 链接 rel 属性名=“属性值”  href 地址 路径-->
</head>	

<body>
	<div class="box">
		
	</div>将

	<p id="box">
		
	</p>
	
	<img src="img/2017-03-20_102041.png"  alt="" width="200px" height="200px">  
	<!-- img 链接   src 地址 路径  alt 报错名=“报错显示”  -->
	<a href="index1.html">跳转
</body>
</html>
*/
/////////////////////









































{/* /* /* /* /* 0321 */ */ */ */ */

html标签分为3类： 
        display: inline-block;/*行内块*/
        display: block;/*块元素*/
        可相互转化

块元素：独占一行，可设置宽高。需加浮动。
	display: block;/*块元素*/
    包含  行内元素+块元素
        div  
        p  
        pre 
        h1-h6 
        <ul>
        <li>1</li>
        </ul>   无序列表


行内元素（内联元素）在一行内显示，没有宽高。 
	display: inline-block;/*行内块*/
		margin值只有左右,没有上下
		不会独占一行
        <span>李虎</span>
        <i></i>
        <strong></strong>
        <em></em>
        font: ;
        b;
        不能包含  块元素
        

行内块元素（内联块元素）   图片就在一行
		不会独占一行
		可以设置宽高
		img   表单元素
        <img src="img/jian.png" width="20" alt="">
        <img src="img/jian.png" width="20" alt="">
        <img src="img/jian.png" width="20" alt="">


盒模型：类似快件一样的东西。所有标签都是一个盒模型
    宽高是实际内容：
    实际宽=border-left+padding-left+width+padding-right+border-right
    实际高=border-top+padding-top+width+padding-bottomt+border-bottom

padding                      内填充
border:20px solid red;       边框
margin-top:20px;             外间距        行内元素margin值只有左右，没有上下。

居中：
position: absolute;
top:50%;
margin-top: -35px;


width: 200px;
height: 200px;
padding:20px;                内填充        行内元素padding值只有左右，没有上下。
padding-top:20px;            宽高是内容区域,
                
padding-right:30px;
padding-bottom:20px;
padding-left:10px;                  margin同理：
padding: 20px 30px 20px 10px;     上、右、下、左。顺时针顺序写
padding： 20px 30px;              上下20px、左右30px；
padding： 20px 30px 40px;         上20px、左右30px、下40px.

border:20px solid red;       边框
margin-top:20px;             外间距        行内元素margin值只有左右，没有上下。

相邻两个兄弟元素的外边距会发生合并，一般布局我们会设定他们的外边距

大部分html元素的盒子属性（margin\padding）默认值为0，有少数html元素的浏览器默认值不为0，例如：body\p\ul\li\form标记等，因此我们有时有必要设置这些属性为0.

margin可以设为负值。padding不可以设为负值。

margin-top的bug问题：当两个容器嵌套时，如果外层容器和内衬容器之间没有别的元素，外层容器没有上边框和padding值是，部分浏览器会把内层元素的margin-top作用与父元素
解决方法：加一个空格。or 给父元素加一个边框。透明边框。



知识点：
1.文档流：从上往下  从左往右 

行内元素在同一行内横向排列
块级元素占满整个一行，在页面中竖向排列

2.浮动
本质：可以横排排列。
height:auto; /* 子元素的高度，就是所有子元素的总高度，子元素撑开的高度 */
weight：auto;/* 父元素的宽度*/
bug：浮动的子元素撑不开父元素（高度为0）
解决方法1：overflow:hidden;    /*超出部分隐藏*/
解决方法2：设置高度！！！
解决方法3：


/* 知识点： */

CSS中：

CSS中是选择器
html中是标签

.box>div{}
.box>.key{}
.box .key{}

text-decoration: none;   去除文字下划线

/*清除默认样式*/
    body{}
    *{
    font-size:  ;
    list-style:none;    /*清除默认样式*/
    margin:0;           /* 选择性填写 */
    padding:0;          /* 选择性填写 */
    }

ul,li{               /* 群组选择器 */
    /*清除默认样式*/
}

img{
	display:block;
}


鼠标移物效果     伪类选择器
.head .right:hover{
    鼠标移动的字
}


border-left: 1px solid red;
border-right: 1px solid red;










































































/* /* /* /* /* 0322 */ */ */ */ */
.background{
	background: red 50px 50px url("../img/3.png") no-repeat fixed;
	/* 1.背景颜色  2.背景定位 3.背景图片 4.重复效果 5.是否随浏览器滚动 */

	/* 背景图片   可并列*/
	background-image: url("../img/1.png"),url("../img/3.png");
	/* 背景图片大小 */
	background-size: 40px 70px,130px 100px;		/*  宽高 */
	background-size: cover;				/*  不变形 等比缩放  覆盖充满全屏*/
	background-size: 300px;				/*  */
	background-size: contain;			/*  不变形 仅一张图片放满屏*/
	/*  背景图片重复 */
	background-repeat: no-repeat,repeat-x;		/*不重复*/
	background-repeat: repeat-x;		/*在X轴重复           默认重复*/
	/*  */
	/* 背景剪切属性 */
	background-clip: content-box;		/* 剪切内容区域 重复*/
	background-clip: padding-box;		/* 剪切内填充区域 	*/
	background-clip: border-box;		/* 剪切边框区域   重复效果都有  默认*/
	/* 背景开始渲染的原点 */
	background-origin:border-box;		/*  从最左边内填充开始渲染 */
	background-origin:padding-box;		/*  						默认 */
	/* 背景定位 */
	background-position : content;	    /* 定位X Y 可为负值 */
	background-position : 20px -20px;	    /* 定位X轴 Y轴  可为负值  左上角为0点*/
	background-position : bottom right;	    /*  方向 定位上下 */
	background-position : center right;	    /*  方向 定位右中 */
	/* 背景跟随页面滚动 */
	background-attachment: scroll;		/* 滚动						默认 */
	background-attachment: fixed;		/* 背景图片固定*/
}

举例：    背景    切图
.bottom .baozhang{
	margin-left: 20px; 
	margin-top: -2px;
	width: 90px;
	height: 43px;
	float: left;
	/* border: 1px solid green; */
	background: url("../img/beijing.png");
	background-position: 0 -675px;
}





overflow: hidden;  /* 超出部分隐藏 */

图片精灵技术：   雪碧图
利用背景图调定位直到调出来。
!!! 做雪碧图时注意定位的数值为负数。









































































































/* /* /* /* /* 0323 */ */ */ */ */

form表单：
1.是WEB浏览器和WEB服务器之间进行通信最常用一种方式。
2.块元素。

3.控件   获取用户所需的信息   不允许出现2个type
4.控件属性：
	type  类型：  
	    text    name  
	            value 默认值
	            size
	            disabled="" 是否可编辑.不可编辑。不写disabled 可直接编辑
	            readonly  只读
	            maxlength   最大长度
	    password  密码
	    radio      单选按钮
	    file      上传文件
	    submit      提交按钮
	    reset       重置
	    button    空按钮
	    textarea   多行的文本输入
	    checkbox    复选框
	    select  option  下拉
	    label       带有两个输入字段和相关标记的简单 HTML 表单：
	                for 属性规定 label 与哪个表单元素绑定。
    -->

<form action="" method="" > <!--method post get -->
    用户名：<input type="text" name="" value="默认值" size="50" disabled="" maxlength="6"><br> <!-- disabled 是否可编辑 -->
    用户名：<input type="text" name="" value="默认值" size="50" maxlength="6"><br>
    密 码： <input type="password"><br>
    性别:<input type="radio" name="sex">男<!-- 单选按钮 -->
         <input type="radio" name="sex">女
         <br>
         <br>
         <br>
    <fieldset>
        <legend>用户信息</legend>
        <label for="">姓名</label> <!-- label 行内元素 for中写ID名 -->
        <input type="text">
    </fieldset>
        <br>
        <br>
        <br>
    复选框
    <input type="checkbox" name="sex" checked="">游泳
    <!-- checked是默认选中的意思 -->
    <input type="checkbox" name="sex">篮球
    <br><br><br>
    下拉
    <select name="" id="">
        <option value="">杭州</option>
        <option value="">上海</option>
        <option value="" selected>北京</option>
        <!-- selected是默认选中的意思 -->
    </select>
    <br><br><br>
    选择文件：<input type="file"><br>
    <input type="submit"><br>
    <input type="reset"><br>
    <input type="button" value="按钮">
    <textarea name="" id="idd" cols="10" rows="3"></textarea>
        <!-- 文本域 列数 行数  定义多行的文本输入文本域不可换行-->
    <br>
    <label for="text">姓名：</label><input id="text" type="text">
    <br>
</form>




<input type="search" class="kuang" placeholder=" 红米4X  小米电视4A 49寸" ><br>
placeholder
搜索框内输入字儿时" 红米4X  小米电视4A 49寸" 会消失











position:

1.position: relative;     
    /* 相对定位 */  相对定位中，原来的位置会被浏览器保留
        相对于本身定位

2.position: absolute;     
    /* 绝对定位 */  是相对拥有相对定位属性的父元素定位的


3.position: fixed;
    /* 固定定位 */  根据浏览器的四个边定位。
4.position: static;
	/* 静态定位 */  默认的定位方式

相对定位是给绝对定位作铺垫，先给父元素定一个位置，再在子元素中利用绝对位置定

4./* 层级 */ 必须在定位上做层级优先
    position: fixed;
    z-index: 10;   

5.	left: 0;
    top: 0;
    right: 0;
    bottom: 0;
    margin: auto;
    /*  上下左右居中 */

    top: 0;
    bottom: 0;
    margin: auto;
    /* 垂直居中 */


举例：
.box .son1{
    display: block;
    width: 404px;
    height: 112px;
    background: red;
    position: relative;
    /* 相对定位 */
    left: 20px;
    top: 40px;
}
.box .son2{
    display: block;
    width: 100px;
    height: 312px;
    background: blue;
    position: absolute;
    /* 绝对定位 */
    left: 20px;
    top: 80px;
}

.box .son3{
    display: block;
    width: 50px;
    height: 612px;
    background: green;
    position: fixed;
    /* 固定定位 */
    left: 20px;
    top: 20px;
    }











  






























































































/* /* /* /* /* 0324 */ */ */ */ */

table	表格  属性：
	tr
		td
		th		标题；默认加粗，居中
		rules
			all; 		线条全部显示
			rows  		行线条显示
			cols 		列线条显示
		align			
			right
			left
			center 		居中
		valign
			top
			middle 		居中
			bottom
		border			表格外边框宽度
		cellpadding		单元格边距
		cellspacing		单元格间距   内边距 
		align			对齐方式
		bgcolor			背景颜色
		rowspan			 竖跨2行   合并行
		colspan			 横跨2列   合并列

border-collapse:collapse
	

/*  */
<tr bgcolor="yellow" align="center"></tr>   /* 行背景色黄色，文字居中 */
<td colspan="2">星期一</td>					/* <!-- 横跨2列   合并列 --> */
<th>01</th>    								/* 标题   默认加粗  */
<td rowspan="2" colspan="2">01</td>			/*  */
tr*10>td{$$}*12     					/* 10行12列 */



/*  举例  */
<table cellpadding="0" border="1" align="center" cellspacing="5" width="569">
	<tr bgcolor="pink">
		  <td colspan="2"  rowspan="2" width="60">星期一</td>
		  <td colspan="2" align="right" valign="middle" ></td>
		  <td colspan="2">星期一</td>
		  <td colspan="2">星期一</td>
		  <th>01</th>
		  <th>02</th>
		  <th>03</th>
	</tr>
</table>























































/* /* /* /* /* 0327 */ */ */ */ */
内容：

一、iframe:		内联子窗口
<div class="main">
        <a href="teacher.html" target="iframe" >小米</a>
        <a href="teacher.html" target="iframe" >百度</a>
      </div>
      <iframe src="" frameborder="1" width="100%" height="100%" name="iframe"></iframe>



二、文本样式： 文本模型   换行规则

<style>
p{
	overflow: hidden;/* 超出部分隐藏 */
	white-space: nowrap;/* 让文字不换行 */
	text-overflow: clip;/* 超出部分剪切 */
	text-overflow: ellipsis;/* 超出部分省略 */
}

英文单词换行:   /*定义换行规则*/
word-break:break-all;
			keep-all;
有 - 的情况下,按-换行,以标点符号换行




三、添加文字图标：  iconfont ok

1.下载的文字文件中，iconfont.css文件放在CSS文件夹中
2. .eot .svg .ttf .woff文件放在新建的iconfont文件夹中
3.修改iconfont.css中地址，添加：../iconfont/。只改“src: url”“url”中的地址。
  最上边不改。
4.设置iconfont.css中文字图标的名字，可改可不改，下边链接用。
5.添加html中链接
	<link rel="stylesheet" href="CSS/index.css">
	<link rel="stylesheet" href="CSS/iconfont.css">
6.设置i
	<i class="iconfont gouwuchekong"></i>
7. 在CSS的.icon-konggouwuche:before { content: "\e601"; }中设置icon的大小颜色

!!!!!注意！！！！     <i class="iconfont gouwuchekong"></i>中是"douwuche"，不是".gouwuche",没有点。



7.设置颜色、大小。font-size     color




四、用户界面：{
1.column:  对象；      OK
	column-count: 2; 
	/* 列数 2列 */
	column-gap: 4em; 
	/* 列与列之间的间距 */
	column-rule: 1px double blue; 
	/* 列与列之间的样式填充   双竖线蓝色隔开 */
	column-fill: auto;
	 /* 平衡列与列之间的高度 */

	/* em */
	font-size: 20px;
	width: 20em;
	/* 把font-size变成原来的20倍 */

	/* rem */
	font-size: 20px;
	width: 20rem;
	/* 根据最上边html的font-size变成原来的20倍 */


2.resize:   拖拽			OK
	overflow: hidden;	前提！！！
	resize: both;
	/* 可拖拽放大框 box */

	resize: vertical;
	/* 竖直方向拖拽 */

	resize: horizontal;
	/* 水平方向拖拽 */


3.box-sizing:   改变盒子模型
	box-sizing: border-box;
	/* 改变盒子模型  加边框和内边距后盒子原本大小不变/*border: 5px solid #000;*/*/
	box-sizing: content-box;
	/*默认情况下。不包含边框和内边距*/
	

4.outline:		轮廓（不占位置） 		OK
	outline: 10px solid red;
	/* 轮廓不占位置 */
	outline-offset: -10px;
	/* 设置与盒子之间的距离 */
	outline: none;
	/* 无轮廓 */


5.border-radius		倒圆角				OK
	border-radius: 10px 20px;         /* 左上右下    左下右上 */
    border-radius: 10px 20px 30px;    /* 左上   左下右上   右下 */
    border-top-left-radius: 50px;		/* 左上   单独对左上设置圆角 */


6.box-shadow		阴影				OK
	box-shadow: 10px 12px 4px 20px red inset;
/*  X轴  Y轴  模糊  阴影（本身大小）  内阴影（不设为外阴影）*/
box-shadow: 0px 5px 20px 3px #ccc;
	box-shadow: 10px 12px 4px 20px red, 10px 12px 4px 20px red inset;
	/*可以设好几重*/
	

7.border-image 		/* 引入边框图片 */			
	border-image-slice: 35;
	/* 裁剪大小 */
	border-image-source: url("border.png");
	/* 引入边框图片 */
	border-image-repeat: round;
	/* 平铺 */
	border-image-repeat: stretch;
	/* 拉伸 */
	border-image-outset: 50px;
	/* 扩散边框，不影响布局 */


8.background:linear-gradient    		渐变			ok
	background: -webkit-repeating-linear-gradient(top,red 20%,blue 70%，green);
	/* 线性渐变       重复（可不写）  到70%时变为纯蓝色*/
	background: -webkit-repeating-linear-gradient(45deg,red 20%,blue 70%);
	                                        /*    方向 角度 */
	background: -webkit-repeating-linear-gradient(top left,red 20%,blue 70%);
	                                        /*    左上 */

	background: -webkit-repeating-radial-gradient(center,red 20%,blue 70%);
	/* 径向渐变       重复（可不写）  到70%时变为纯蓝色*/
background: -webkit-linear-gradient(top,#F6F6FE 20%,#fff 70%);
/*从顶部开始变色*/
	background: hsl(120, 50%, 50%)      
	/* 工业用色   h 色调（0-360） s 饱和度（0%-100%） l 亮度（0-100%）*/


9.倒影
	.box1{-webkit-box-reflect: below 1px -webkit-linear-gradient(top, rgba(0,0,0,0),rgba(0,0,0,1));}
	/* 上下左右 投影+渐变虚化 */ /* above 上 below 下  20px 投影和本体的距离*/  过渡效果
							/* below 20px url(uek.png)  必须是png格式，镂空图片*/





10.  度  透明色
background: rgba(0, 0, 0, 0.8);
            /*  背景的透明色 */

background: rgb(0, 0, 0);
            opacity: 0.8;
/* 透明度0-1  调整整个box，包括字体，边框的透明度会降*/


.a{
	opacity: 0;
	transition: all 1s;
	}
.a:hover{
	opacity: 1;
	}
鼠标移动过去过1秒显示




11.过渡
	transition: all 1s linear;
	/* 监测 all 所有  background 背景 */
	transition-property: all ;
	/* 样式变化  all 所有都变    background 背景变化 */
	/* transition: all ; */
	transition-duration:  3s;
	/* 持续时间 */
	transition-timing-function: ease;
	/* 动画效果  从慢到快 从快到慢  ease-in    ease-out    linear 线性、匀速*/
	transition-delay: 1s;
	/* 延时1s */


transition: all 2s ease;
监测放在.box{本体}本体中时，鼠标移物会动，移走以后会变化

放在.box：hover{}中时，鼠标移物会动，移走以后不会变化




12.旋转
	transform: rotate(720deg);       
    /* 2D旋转 deg度数   rad弧度 */
/* 浮动  Y轴*/
	transform: translateY(-10px);

	transform-style: preserve-3D; /* 保持3D效果 */






13.平移 {
transform: translateY(-10px);
/* 平移 translateX  translateY*/




知识点：



画布：http://able-fan.github.io/canvas/ 

视频连接：		autoplay自动播放	
video方式：
<video controls="controls" autoplay="autoplay">
  <source src="movie.ogg" type="video/ogg" />
  <source src="movie.mp4" type="video/mp4" />
</video>

视频连接：
youku--打开视频--分享--复制html
<embed src='http://player.youku.com/player.php/sid/XMjY2MTAyMDQ4MA==/v.swf' allowFullScreen='true' quality='high' width='480' height='400' align='middle' allowScriptAccess='always' type='application/x-shockwave-flash'></embed>





<time></time>
<br>
进程：<progress> </progress>
<br>
视频：
autoplay
<br>
<video controls="controls" autoplay="autoplay">
  <source src="movie.ogg" type="video/ogg" />
  <source src="movie.mp4" type="video/mp4" />
Your browser does not support the video tag.
</video>

<embed src='http://player.youku.com/player.php/sid/XMjY2MTAyMDQ4MA==/v.swf' allowFullScreen='true' quality='high' width='480' height='400' align='middle' allowScriptAccess='always' type='application/x-shockwave-flash'></embed>









/* /* /* /* /* 0327 */ */ */ */ */



2D特效：				OK
	transform: rotate(45deg);
	/* 旋转   deg角度  red（2π）弧度 */

	transform: translateY(-10px);
	/* 平移 translateX  translateY*/

	transform: skew(45deg, 45deg);
	/* 斜切   skewX  skewY*/

	transform: scale(0, 0);
	/* 缩放 scaleX  scaleY */

	transform-origin:50% 50%;

	transform-origin:top left;
	/* 定义原点、零点位置 */

	transform: translate(30px, 30px) scale(0, 0);
    /* 平移+缩放 */












/* /* /* /* /* 0328 */ */ */ */ */
3D特效：


/* 场景 */
	.perspective{
	    width: 300px;
	    height: 150px;
	    border: 1px solid #000;
	    margin: 0 auto;
	    perspective: 800px;
	    perspective-origin: 50% 50%;
	    /* 默认原点在中间位置 */
	    }

	.perspective .box3{
	    width: 200px;
	    height: 200px;
	    background: green;
	    margin: 100% auto;
	    transform-origin:top left;
	    transition: all 1s ease;
	    }
	.perspective .box3:hover{
	    transform: rotate3d(720deg);
	    transform: rotate3d(1, 1, 0, angle)(720deg);
	    /* 向量  角度 */
	    transform: rotate3d(1, 1, 0, 720deg);
	    /* X Y Z 角度 */
	    transform: scale3d(0, 0, 0);
	    /* 3D缩放 */




 /* 定义一条动画规则 */
.neirong11-1>.pic1>img{
	animation-name: animation1;
	animation-play-state: running;
	/* 进去直接播放 */
	animation-iteration-count: infinite;
	/* 动画 无限播放次数 */
	animation-duration: 1s;
	/* 必须 动画时间 */
	animation-timing-function: linear;
}
@keyframes animation1{
		0%{
		    transform: rotate(0deg);
		}
		100% {
		    transform: rotate(360deg);
			}
		}
		
 /* 定义一条动画规则 */

	animation-name: animation1;
	/* 必须 动画名称 */
	animation-duration: 1s;
	/* 必须 动画时间 */
	animation-timing-function: ease;
	/* 必须 动画方式 */
	animation-delay: 1s;
	/* 必须 延迟 */
	animation-iteration-count: 2;
	/* 动画 播放次数 */
	animation-iteration-count: infinite;
	/* 动画 无限播放次数 */
	animation-direction: alternate;
	/* 动画 逆向播放 占1个播放次数，需和播放次数配合使用*/
	animation-play-state: running;
	/* 进去直接播放 */
	animation-play-state: paused;
	/* 进去播放停止 */


/* 定义新的动画规则 */
	@keyframes animation1{
		from {
		    width: 200px;
		    height: 500px;
		}
		to {
		    width: 500px;
		    height: 200px;
			}
		}

/* 定义新的动画规则 多个动画*/
    @keyframes animation1{
        0%{
            width: 200px;
            height: 500px;
        }
        50%{
            width: 500px;
            height: 200px;
        }
        100%{
            width: 500px;
            height: 200px;
        }
    }








CSS选择器：

/* /* /* /* /* CSS1 */ */ */ */ */
 
第5个之后所有的div。
.box>div:nth-child(5)~div{
	margin-top: 10px;
}


a标签的顺序：
a.link{
    color: red;
}
/* 最开始红色 */
a.visited{
     color: blue; 
}
/* 访问后变蓝色 */
a.active{
    color: green;
}
/* 点击时变绿色 */




/* 对li的第一个子元素操作 */
.box1 ul li:first-child{ background: blue; }

/* 对li的第三个子元素操作 */
.box1 ul li:nth-child(3){ background: blue; }

/* 对li的倒数第2个子元素操作 */
.box1 ul li:nth-last-child(2){ background: blue; }

<div class="box1">
    <ul>
        <li>01</li>
        <li>02</li>
        <li>03</li>
        <li>04</li>
        <li>05</li>
        <li>06</li>
    </ul>





/* 对所有有"col-"的都向左浮动： */

[class*="col-"]{
	float: left;
}

.col-xs-1{
	width:8.33333% ;
}
.col-xs-2{
	width:16.66666% ;
}
.col-xs-3{
	width:24.99999% ;
}
.col-xs-4{
	width:33.33333% ;
}
.col-xs-5{
	width:41.66666% ;
}





























/* /* /* /* /* 0329 */ */ */ */ */


一、内容
1.响应式：一个页面可以兼容不同的终端
@media screen and (max-width: 400px)
注意隐藏

2.先小屏，后中屏,再大屏
@media screen and (max-width: 500px)

@media screen and (max-width: 800px)

3.在响应式设计中，不给div重新设计的话有可能会继承最原始的参数。
margin-bottom: 1px;
margin-top: 1px;
margin-right: 0;
margin-left: 0;

4.
@media screen and (max-width: 100%)
当宽度自由时，无进度条



5.链接
<link rel="stylesheet" href="css/index.css" media="screen and (max-width:600px)" />

example：

.box .son{
	width: 20%;
	/* 先设置子元素占屏幕的大小百分比 */
	height: 400px;
	border: 2px solid #000;
	float: left;
	box-sizing: border-box;
	background: blue;
}

@media screen and (max-width: 800px){
	.box .son:nth-child(3){
		display: none;
	}
	.box .son:nth-child(2){
		width: 40%;
		/* 设置子元素占屏幕的大小百分比 */
		background: red;
	}
	.box .son:nth-child(1){
		width: 40%;
		background: red;
	}
}

@media screen and (max-width: 600px){
	.box .son:nth-child(2){
		display: none;
	}
	.box .son:nth-child(3){
		display: none;
	}
	.box .son:nth-child(1){
		width: 80%;
		background: yellow;
	}
}





2.两端对齐
nav .con1{
	text-align: justify;
}

nav .con1 a{
	display: inline-block;
	/* 行内块元素   针对汉字，不让汉字分开 */
}

nav .con1:after{
	content: "";
	display: inline-block;
	/* 两端对齐默认给最后加了一行 */
	height: 0;
	width: 100%;
}





















/* /* /* /* /* 0330 */ */ */ */ */

十二栅格化

十二栅格化响应中加普通响应达到效果

各种屏的

@num1 <768px 超小屏（手机端） 
	  >=768px 小屏（iPad）
@num2 >=992px 中屏 桌面浏览器
@num3 <1200px  大屏 大桌面浏览器


/* 两种方式 */
/* 百分比 通屏的 */ 流式
.container-fiuld{
	width:100% ;
	height: auto;
	margin:0 auto ;
}

/* 固定宽度 */
.container{
	margin: 0 auto;
}


2.先小屏，后中屏,再大屏
@media screen and (max-width: 500px)

@media screen and (max-width: 800px)

2.1
/* 小屏 min  不小于 也就是大于*/
@media screen and (min-width:768px)

/* 中屏 min  不小于 也就是大于*/
@media screen and (min-width:992px)

/* 大屏 min  不小于 也就是大于*/
@media screen and (min-width:1200px)

/* 超小屏 */
@media screen and (max-width:768px)





/* 所有有"col-"的都向左浮动 */
[class*="col-"]{
	float: left;
}

对某一个元素隐藏。
.col-md-hid{
		display:none;
	}
/* 超小屏 */
@media screen and (max-width:768px){
	.container{
		width: 768px;
	}
	.col-xs-1{
		width:8.33333% ;
	}
	.col-xs-2{
		width:16.66666% ;
	}
	.col-xs-3{
		width:24.99999% ;
	}
	.col-xs-4{
		width:33.33333% ;
	}
	.col-xs-5{
		width:41.66666% ;
	}
	.col-xs-6{
		width:50% ;
	}
	.col-xs-7{
		width:58.33333% ;
	}
	.col-xs-8{
		width:66.66666% ;
	}
	.col-xs-9{
		width:75% ;
	}
	.col-xs-10{
		width:83.33333% ;
	}
	.col-xs-11{
		width:91.66666% ;
	}
	.col-xs-12{
		width:100% ;
	}
}




<style>
    .box div{
        height: 200px;
        border: 1px solid #000;
        box-sizing: border-box;
    }
</style>

<body>
	<div class="box container">
		<div class="col-xs-1 col-sm-2 col-md-4 col-lg-6"></div>
        <div class="col-xs-1 col-sm-2 col-md-2 col-lg-2"></div>
        <div class="col-xs-1 col-sm-2 col-md-2 col-lg-2"></div>
        <div class="col-xs-1 col-sm-2 col-md-2 col-lg-2"></div>
	</div>
</body>


HELLO WORD！！！！ 十二栅格化 

都不设置宽，文字不设置高。
大盒子宽为100%。
里面的不设置。
在@media screen and (min-width:768px)中
设置的为 
在min中的宽要设成768px 992  768，
在max中宽度要设成100%。


 <footer>
    <div class="box container-fiuld">
        <div class="box1 col-xs-12 col-sm-12 col-md-4 col-lg-4">
            <h1>Heading</h1>
            <span>Donec id elit nonlesuada magna mollis euismod. Donec sed odio dui.</span>
            <a href="">View Details》</a>
        </div>
        
        <div style="color:red" class="box1 col-xs-12 col-sm-12 col-md-4 col-lg-4">
            <h1>Heading</h1>
            <span>Donec id elit non mi porta gravida at eget metus. Falesuada magna mollis euismod. Donec sed odio dui.</span>
            <a href="">View Details》</a>
        </div>
        
        <div class="box1 col-xs-12 col-sm-12 col-md-4 col-lg-4">
            <h1>Heading</h1>
            <span>Donec id elit non malesuada magna mollis euismod. Donec sed odio dui.</span>
            <a href="">View Details》</a>
        </div>
        
        <div class="di container-fiuld"><span  class="col-sm-12 col-md-12 col-lg-12"></span> © 2016 Company, Inc.</div>

    </div>
</footer>











/* /* /* /* /* 0331 */   HBuilder  */ */ */ */


JS快捷键：
ctcl + shift +B  注释

//  ========== 
//  = Banner = 
//  ========== 


查看电脑本机IP，  cmd-->ipconfig-->ipv4-->192.168.1.143

移动端测试方式：
1.Chrome方式：审查元素 移动端测试环境
			  智能测试尺寸，
2.HBuilder  有线-->USB-->HBuilder 中显示。

3.wampserver 64 -->右键 --> 语言-->Chinese 
			左键-->www 目录-->把文件拖进去-->
			
 	手机连接：手机浏览器里输入192.168.1.143/移动端
			
4.设置WEB服务器-->外部WEB服务器设置-->新建-->http://192.168.1.143:8020-->确定
   -->HTML类-->选择http://192.168.1.143:8020-->确定-->打开-->视图-->查看视图-->WEB浏览器-->手机浏览器扫二维码
   
5.手机找不到要打开的文件
打开manifest.jason
选择页面。修改即可


layout viewport 布局视口
一搬宽度为980px,可通过document.documentElement.clientWidth获取


layout viewport 视觉视口


idea viewport 理想视口


<!--默认-->
    <meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta name="apple-mobile-web-app-capable" content="yes">
    
    <meta name="viewport" content="width=device-width,initial-scale=1.0,maxmum--scale=1.0,user-scalable=0"/>
  
    <!--默认结束-->









/* /* /* /* /* 0401 */ */ */ */ */


◆技巧◆
alert(1);/*弹出框*/
◆技巧◆
/*transform: translate3d(0, 0, 0);*/
会让背景默认为灰色

/*UI设计师给的尺寸*/
	设计尺寸             设备尺寸                     font-size(倍数=设备尺寸÷设计尺寸*100)
	750px      375px      7.50rem*倍数                          50px
	300px      150px      3.0rem*倍数			     50px

html{
	font-size: 50px;/*(设备尺寸÷设计尺寸*100)*/
}
.box{
	width: 2rem ;
	height: 2rem;
	background: red;
	font-size: 12px;
	}  




JS的默认格式：

//  ========== 
//  = 移动端HTML中head： 
//  ========== 
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
    <!--    -->
    <meta name="x5-orientation" content="portrait | landscape" />
    <meta name="screen-orientation" content="portrait">
    <meta name="x5-fullscreen" content="true" />
    <meta name="full-screen" content="yes">
    <meta name="format-detection" content="telephone=no, email=no" />
    <!---->
    <title>天猫</title>
    <link rel="stylesheet" href="css/tianmao.css" />
    <link rel="stylesheet" href="css/iconfont.css" />
    <script src="js/tianmao.js"></script>
</head>



//  ========== 
//  = JS文件中：JS的默认格式  = 
//  ========== 

'use strict'

//窗口加载完后执行一段程序

alert(1);/*弹出框*/

window.onload = function(){ /*定义函数*/
	var designWidth = 375; /*定义设计尺寸.只改设计尺寸为1080，其他都是从PS上量的尺寸除以100即可*/
	
	function fontsize(){
		var CW = document.documentElement.clientWidth;     
		/*  CW变量 设备尺寸 文档的宽 */
		console.log(CW);   /*输出文档的宽度*/
		var size = CW/designWidth*100+"px";
		document.querySelector("html").style.fontSize = size; 
		/* 设置html的 font-size */
		
		console.log(size);/*打印*/
	}
	
	fontsize();/* 运行此函数 */
	alert(5);
	window.onresize = fontsize; /* 监测窗口尺寸是否发生改变 */ 
}





//  ========== 
//  = 移动端CSS文件中/*清除默认样式*/  = 
//  ========== 

*{
	margin: 0;
	padding: 0;
	list-style: none;
	/*font-size: 12px;*/
	-webkit-tap-highlight-color: rgba(0,0,0,0);
	-webkit-appearance: none;/*安卓不支持*/
	-webkit-text-size-adjust: 100%;
	-webkit-user-select: none;	
	-webkit-overflow-scrolling: touch;
	<a href="tel:110">请拨打电话110</a>
	<a href="mailto:qq@.com">请发送邮件qq@.com</a>
	-webkit-user-select:none;user-select:none;
	-webkit-tap-highlight-color:rgba(255,255,255,0);
	-webkit-text-size-adjust: 100%;
	text-size-adjust: 100%;
	-webkit-transform: translate(0,0,0);
	transform: translate3d(0, 0, 0);
}
html, body, form, fieldset, p, div, h1, h2, h3, h4, h5, h6 {-webkit-text-size-adjust:none;}
body {-webkit-overflow-scrolling:touch; overflow-scrolling: touch;}
p{max-height:9999999px}


body{
	font-family: helvetica;
}

img{
	display: block;
}

a{
	text-decoration: none;
}
html{
	font-size: 100px;
	/*定义倍数*/
}












/* /* /* /* /* 20170405 */ */ */ */ */

弹性化布局    flex
技巧：
子元素的两个块居中对齐
justify-content: center;

弹性化布局
flex 容器    
//项目
/*父元素中设置*/
.fuyuansu{
	flex-wrap: wrap;
	flex-direction: row;
	justify-content:center;
	align-content: space-around;
}
/*子元素中设置*/
.ziyuansu{
	width: (固定宽高);
}




/* 知识点 */
.box{
    
    display:-webkit-box; (旧版)
	display: flex; //(新版)
//渐变--兼容问题
//先写兼容，最后写标准。
  }

用flex之后，浮动失效
display: -webkit-flex;
display: flex;
display: inline-flex;  //行内元素


####★技巧★   flex:1;

父 容器   display:flex
子项目：		flex:1;     
			flex:2;

设置字体：
justify-content: flex-end;
align-items: flex-end;


行内块元素的时候：
display:inline-flex
	flex: ;	/* 容器 */
	display: flex;
	/* 排列方向 */
	flex-direction: row;/* 横排 */
	/*row  column  row-reverse column-reverse 横排   竖排  从右到左   从下到上  */
	
	flex-wrap: wrap-reverse;/* 包裹方式 换行 */
	/* wrap  nowrap wrap-reverse 垂直方向反向*/

	justify-content: space-around;/* 主轴对齐方式 */
	/*  flex-start 开始位置对齐  
		flex-end  结束位置对齐
		center  居中  
		space-between; 两端对齐，项目之间的间隔都相等。
		space-around：每个项目两侧的间隔相等。  */

align-items: flex-start;/* 交叉轴对齐方式 */
	/* flex-start; center 居中 flex-end; 居下
	baseline 项目的第一行文字的基线对齐*/
align-items:stretch   默认占满整个容器。但高度不设置或设置为auto的时候。

align-content: space-around;/* 多行对齐 */
	/* flex-start 开始位置对齐  
		flex-end  结束位置对齐
		center  居中  
		space-between; 把剩余部分平均分到两边
		space-around; */
align-content:stretch   默认占满整个容器。但高度不设置或设置为auto的时候。


	项目顺序：
item:
	/* 数值越小，排列越靠前，默认为0。 */
	order: 1;
	order: 2;

	兼容写法：
	-webkit-box-ordinal-group: 1;

	


	项目占比（放大）：
flex-grow:0;
	默认将剩余空间占满
默认值为0，即使存在剩余空间也不会放大

	当 flex-grow:1;中有一个 flex-grow:2; 时，flex占的空间大一倍
	



	项目缩小
flex-shrink: ;
	默认值为0，即使存在剩余空间也不会缩小


	项目所占空间大小: 
flex-basis: 300px;


	项目自己的对齐方式: 
	align-self: auto | flex-start |flex-end | center | baseline | stretch ;


	兼容写法：
	-webkit-box-orient: horizontal | vertical;

	-webkit-box-decoration: normal | vertical;

	-webkit-box-pack: start | end | center | justify;









用户名：liujiang135

lantern  翻墙下载
/* /* /* /* /* ０４１０ */ */ */ */ */
桌面版  http://desktop.github.com/



上传git 文件

<1>  cd 文件夹的地址
	cd C:\Users\Administrator\Desktop\liujiang135

<2>  git clone 去github上复制浏览器的网址

<3>  把文件放进去

<4>  cd 新的文件夹地址

	//在文件夹右击--gitbash-->  git add

<5>  git add .                        (1)
	(上传的文件必须有index.html)

<6>  git status   (2)

<7>  git commit -m"uek1.0-20170410"   (3)

	git commit -m"uek5"
	
<7.1>	git pull  //团队项目，同步    //可省         (3.1)
	当有人把项目改了之后，需要pull一下
	
	复制它上边的 名字、email，改成自己的。                           //可省   (3.2)
	git config --global user.name "jiangtop"                    //可省   (3.2)
	git config --global user.email "1392534029@qq.com"          //可省   (3.2)

<8>上传之前 先跑这行代码                   (4)
git config http.postBuffer 524288000

<9>  git push                         (5)
推送

setting-->githup page-->source-->none-->改成master branch-->改成none-->改成master branch--反复几次.最后点source 右上角的网址就是.


下载:
git clone git:C:\Users\Administrator\Desktop\git\123


添加好友
github主页--> search --> 输入名字 --> users --> follow





github-->找到老师的文件-->右上角fork-->clone 地址--> new pull request -->creat pull request



















/* /* /* /* /*　规范　 */ */ */ */ */

CSS书写顺序
　　1.位置属性(position, top, right, z-index, display, float等)
　　2.大小(width, height, padding, margin)
　　3.文字系列(font, line-height, letter-spacing, color- text-align等)
　　4.背景(background, border等)
　　5.其他(animation, transition等)


CSS书写规范
　　使用CSS缩写属性
　　CSS有些属性是可以缩写的，比如padding,margin,font等等，这样精简代码同时又能提高用户的阅读体验。


去掉小数点前的“0”


简写命名
　　很多用户都喜欢简写类名，但前提是要让人看懂你的命名才能简写哦！

16进制颜色代码缩写
　　有些颜色代码是可以缩写的，我们就尽量缩写吧，提高用户体验为主。

连字符CSS选择器命名规范
　　1.长名称或词组可以使用中横线来为选择器命名。
　　2.不建议使用“_”下划线来命名CSS选择器，为什么呢？
输入的时候少按一个shift键；
浏览器兼容问题 （比如使用_tips的选择器命名，在IE6是无效的）
能良好区分JavaScript变量命名（JS变量命名是用“_”）

不要随意使用id
　　id在JS是唯一的，不能多次使用，而使用class类选择器却可以重复使用，另外id的优先级优先与class，所以id应该按需使用，而不能滥用。

为选择器添加状态前缀
　　有时候可以给选择器添加一个表示状态的前缀，让语义更明了，比如下图是添加了“.is-”前缀。

CSS命名规范（规则）
　　常用的CSS命名规则
　　头：header
　　内容：content/container
　　尾：footer
　　导航：nav
　　侧栏：sidebar
　　栏目：column
　　页面外围控制整体佈局宽度：wrapper
　　左右中：left right center
　　登录条：loginbar
　　标志：logo
　　广告：banner
　　页面主体：main
　　热点：hot
　　新闻：news
　　下载：download
　　子导航：subnav
　　菜单：menu
　　子菜单：submenu
　　搜索：search
　　友情链接：friendlink
　　页脚：footer
　　版权：copyright
　　滚动：scroll
　　内容：content
　　标签：tags
　　文章列表：list
　　提示信息：msg
　　小技巧：tips
　　栏目标题：title
　　加入：joinus
　　指南：guide
　　服务：service
　　注册：regsiter
　　状态：status
　　投票：vote
　　合作伙伴：partner


id的命名:
　　1)页面结构
　　容器: container
　　页头：header
　　内容：content/container
　　页面主体：main
　　页尾：footer
　　导航：nav
　　侧栏：sidebar
　　栏目：column
　　页面外围控制整体佈局宽度：wrapper
　　左右中：left right center
　　(2)导航
　　导航：nav
　　主导航：mainnav
　　子导航：subnav
　　顶导航：topnav
　　边导航：sidebar
　　左导航：leftsidebar
　　右导航：rightsidebar
　　菜单：menu
　　子菜单：submenu
　　标题: title
　　摘要: summary
　　(3)功能
　　标志：logo
　　广告：banner
　　登陆：login
　　登录条：loginbar
　　注册：register
　　搜索：search
　　功能区：shop
　　标题：title
　　加入：joinus
　　状态：status
　　按钮：btn
　　滚动：scroll
　　标籤页：tab
　　文章列表：list
　　提示信息：msg
　　当前的: current
　　小技巧：tips
　　图标: icon
　　注释：note
　　指南：guild
　　服务：service
　　热点：hot
　　新闻：news
　　下载：download
　　投票：vote
　　合作伙伴：partner
　　友情链接：link
　　版权：copyright


CSS样式表文件命名
　　主要的 master.css
　　模块 module.css
　　基本共用 base.css
　　布局、版面 layout.css
　　主题 themes.css
　　专栏 columns.css
　　文字 font.css
　　表单 forms.css
　　补丁 mend.css
　　打印 print.css
``` 

