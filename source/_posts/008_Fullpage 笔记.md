---
title: 008- Fullpage
---


## Fullpage
 
```bash
##   sectionsColor  //设置背景颜色
	sectionsColor:['green','orange','red','lime'];
可以为每一个section设置background-color属性


##   controlArrows:   定义是否通过箭头来控制slide幻灯片，
默认为true，当我们设置为false，则幻灯片左右的箭头消失，在移动端上我们可以通过滑动来控制幻灯片

##   continuousVertical	   是否循环滚动
布尔值	false	是否循环滚动，与 loopTop 及 loopBottom 不兼容

##   设置自动循环延时
	setInterval(function(){
	 	$.fn.fullpage.moveSectionDown();
	 },2000)

##   afterLoad  滚动到某一屏后的回调函数，
接收 anchorLink 和 index 两个参数，anchorLink 是锚链接的名称，index 是序号，从1开始计算
	afterLoad: function(anchorLink, index){
		if(index == 2){
			$('.section2').find('p').delay(500).animate({
				left: '0'
			}, 1500, 'easeOutExpo');
		}
	},
*	滚动到某一屏执行的动作
*	
##   onleave   滚动前的回调函数，
接收 index、nextIndex 和 direction 3个参数：
	index 是离开的“页面”的序号，从1开始计算；
	nextIndex 是滚动到的“页面”的序号，从1开始计算；
	direction 判断往上滚动还是往下滚动，值是 up 或 down。

	onLeave: function(index, direction){
		if(index == '2'){
			$('.section2').find('p').delay(500).animate({
				left: '-120%'
			}, 1500, 'easeOutExpo');
		}
	}
*	就是滚动到第3屏后，让第二瓶的东西再隐藏掉，和afterLoad配合使用
*	
##   anchors   数组 定义锚链接
	html:  <button><a href="#page1">按钮1</a></button>
	JS:  anchors:['page1','page2','page3','page4'],

##	navigation	是否显示项目导航   (轮播点  右边圆圈圈)   
	'navigation':true,
布尔值	false	

##   navigationPosition	字符串	right	项目导航的位置，可选 left 或 right
	'navigationPosition':'left',

##	navigationColor	字符串	#000	项目导航的颜色    
无效。解决方法
	`#fp-nav ul li a.active span,  
	.fp-slidesNav ul li a.active span {  
	    background: #fff; /*这里设置的是活动导航的颜色*/  
	}  
	`#fp-nav ul li a span,  
	.fp-slidesNav ul li a span {  
	    border: 1px solid #fff;/*这里设置的是非活动导航的颜色*/  
	}  

##   navigationTooltips	数组	空	项目导航的 tip   导航小圆点的提示，注意按顺序设置
	navigationTooltips:[‘page1‘,‘page2‘,‘page3‘,‘page4‘,‘page5‘],
	'navigationTooltips':['page1','page2','page3','page4'],


##   showActiveTooltip是否显示当前页面的tooltip信息，默认为false
showActiveTooltip:true,

##   slidesNavigation 是否显示横向幻灯片的导航，默认为false
slidesNavigation:true,
	
##   slidesNavPosition横向导航的位置，默认为bottom，可以设置为top或bottom
slidesNavPosition:'top',
	
##   controlArrowColor:'red',   左右滑块的箭头的背景颜色
##  
             
            //
            
            //
            slidesNavPosition:'top',
            //左右滑块的箭头的背景颜色
            controlArrowColor:'red',
##   
##		 //配置项介绍

//sectionsColor为每个section设置background-color属性
	sectionsColor:[‘green‘,‘orange‘,‘gray‘,‘red‘,‘yellow‘],

//controlArrows定义是否通过箭头来控制slide,默认true
	controlArrows:false,

//verticalCentered定义每一页的内容是否垂直居中，默认true
	verticalCentered:false,

//anchors定义锚链接，默认为[],定义锚链接时，值不要和页面中的任何ID或name相同，且不需要加#
	anchors:[‘page1‘,‘page2‘,‘page3‘,‘page4‘,‘page5‘],

//loopTop滚动到最顶部后是否连续滚动到底部，默认为false
//loopBottom滚动到最低部后是否连续滚动到顶部，默认为false
##  continuousVertical	   是否循环滚动
和它冲突
//loopHorizontal横向slide幻灯片是否循环滚动，默认为true  ？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？无效



##		？？？？？？？？？？？？？？？？？？？？？？？？？
//resize字体是否随窗口缩放而缩放，默认false
	resize:true,

//scrollingSpeed设置滚动速度，单位毫秒，默认700
	scrollingSpeed:1000,



//lockAnchors是否锁定锚链接，默认为false,设为true后链接地址不会改变
	lockAnchors:true,

//easing定义页面section滚动的动画方式，默认为easeInOutCubic,若修改此项需引入jquery.easing插件

//css3是否使用CSS3 transforms来实现滚动效果，默认为true。若浏览器不支持CSS3，则会用Jquery来实现
//css3:false,



//autoScrolling是否使用插件的滚动方式，默认为true,若为false则会出现浏览器自带滚动条    
//scrollBar是否包含滚动条，默认为false,若为true浏览器自带滚动条出现
//paddingTop/paddingBottom设置每一个section顶部和底部的padding,默认为0
//fixedElements固定元素，默认为null,需要配置一个jquery选择器，在页面滚动时，fixElements设置的元素不滚动
fixedElements:"#header",
//keyboardScrolling是否可以使用键盘方向键导航，默认为true
//touchSensitivity在移动设备中滑动页面的敏感性，默认为5最高100，越大越难滑动
//continousVertical是否循环滚动，默认为false,注意这个属性和loopTop loopBottom不兼容，不能同时设置

//animateAnchor锚链接是否可以控制滚动动画，默认为true,若为false则锚链接定位失效
//recordHistory是否记录历史，默认为true,通过浏览器的前进后退来导航。若设置autoScrolling:false,那么这个属性将被关闭
//menu绑定菜单，设定的相关属性与anchors的值对应后，菜单可以控制滚动条，默认为false。可设置为菜单的jquery选择器
//menu:"#fullpageMenu",
//navigation是否显示导航，默认为false
            navigation:true,   
##   
##   
##   
	$("img.lazy").lazyload({effect: "fadeIn"}),
```