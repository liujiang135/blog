---
title: 003_JQuery 移动端
---
 

## JQuery

```bash
####★技巧★
####★技巧★
####★技巧★
####★技巧★
####★技巧★   
单词：	trigger  触发

####★技巧★   图片按需加载
 $('img.lazy').load();

####★技巧★
fast:600ms
normal:400ms
slow:200ms

####★技巧★
let point = $('.point').get(0)
相当于 point = $('.point')[0]

####★技巧★    css
div[class = input]{ 样式 }

####★技巧★   p标签不能嵌套其他标签
p标签作为最内层的标签

####★技巧★  注意有没括号 ()
a.height() 

####★技巧★  获取div
let box = $('div')
    let box = $(':empty')
    let box = $('div:first-child')

####★技巧★
兼容 + webkit

####★技巧★
常改的图片用   img,不改的用背景图片，图片精灵

####★技巧★
wamp

www  目录

把文件放进去

localhost/wui1611/index.html

手机电脑连相同的网

手机输入 192.168.1.1

####★技巧★    添加类名  移除类名
	lis.addClass('active')
    lis.removeClass('active')

####★技巧★
<marquee scrolldelay="100">高婧太厉害了666</marquee>
<marquee scrollamount="15" >&nbsp;&nbsp;&nbsp;给高婧送个别墅(^-^)</marquee>
<marquee>再送辆跑车</marquee>
<marquee scrollamount="30" >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;999朵鲜花+一个火箭</marquee>


####★技巧★  队列
	入队   出队
  1  2  3  4  5  6  7  8  9  0
####★技巧★
####★技巧★
####★技巧★   获取$('.box')   注意  .  [0] 

####★技巧★   CSS布局
height:auto;
高度自动，靠内部元素撑开

####★技巧★   清除默认行为
 $(document).mousedown(false);

####★技巧★    JS移动端调用
/*UI设计师给的尺寸*/
	设计尺寸             设备尺寸                                                font-size(倍数=设备尺寸÷设计尺寸*100)
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

##★技巧★   const a = 750;   声明变量
*	值不能改
*	必须同时赋值

	const  A = 'a'  不能改
	const  arr = [1,2,3,4]  数组能改
	arr.push[5,6,7]

PC端事件会比移动端延迟300ms
click  要比 touch 延迟300ms



##	点透
	在box上面放一个 a链接， 点击a链接时，a链接执行跳转，如果长按a链接，再放开，a链接不会跳转


e.toucher   
	当前事件触发时，屏幕上检测到几个手指头。  记录几个手指头在屏幕上
targetTouches
	当前事件触发时，这个元素上检测到几个手指头。  记录几个手指头在元素上
changeToucher
    当前事件触发时，几个手指头执行了这个事件。  记录几个手指头涉及到当前事件

###  事件：
*	touchstart:     //手指放到屏幕上时触发
*	touchmove:      //手指在屏幕上滑动式触发
*	touch
*	:    //手指离开屏幕时触发
*	touchcancel:     //系统取消touch事件的时候触发，这个好像比较少用

###  跟踪触摸的属性
*	touches:     //当前屏幕上所有手指的列表
*	targetTouches:      //当前dom元素上手指的列表，尽量使用这个代替touches
*	changedTouches:     //涉及当前事件的手指的列表，尽量使用这个代替touches
*	`let ev = e.changedTouches[0];`

###  触摸事件的属性
*	clientX / clientY:      //触摸点相对浏览器窗口的位置
*	pageX / pageY:       //触摸点相对于页面的位置
*	screenX  /  screenY:    //触摸点相对于屏幕的位置
*	identifier:        //touch对象的ID
*	target:       //当前的DOM元素
*	

##	移动端布局规范：
	<header>顶部</header>
	<main>主体</main>
	<footer>底部</footer>






#   Jquery

##	支持链式调用、隐式循环
不停的点下去

##***选择器***

###   ancestor descendant  
在给定的祖先元素下匹配所有的后代元素
	$("form input")   找form下多有的Input

###   parent > child
	$("form > input")   找form的子元素中的input。input是form的子元素
 
###   prev + next
	$("label + input")   找在label后边的input。同级关系

###   prev ~ siblings
	$("form ~ input")  找与form同辈的所有input.同级关系

###   :not(selector)
除selector以外的
	$("input:not(:checked)")

###   :eq(index)    匹配一个给定索引值的元素  从0开始
	$("tr:eq(1)")	查找第二行

###   :gt(index)	大于index的    从 0 开始计数
###   :lt(index)					从 0 开始计数
	$("tr:gt(0)")

###   :header	匹配如 h1, h2, h3之类的标题元素
	$(":header").css("background", "#EEE");

###   :animated		匹配所有正在执行动画效果的元素

###   
###   
###   
###   
###   
###   p标签里没出现过套用p标签

###   :first	获取第一个元素    
	$('li:first');		li必须是ul中的第一个子元素，否则无法获得

###	  :first-of-type     找同类中的第一个
*	结构化伪类，匹配E的父元素的第一个E类型的孩子。
*	等价于:nth-of-type(1) 选择器
$("span:first-of-type");      找第一个span。可以不是第一个子元素

###   
###   
###   
###   




##  筛选

### 过滤：
$("p").eq(1)

### <1>  eq(index|-index)   可以是负数，倒数第一     从0开始
	$('li').eq(0)   先选所有的li,再选li中的第一个
	$('li').eq(-1)   倒数第一个

### <2>  hasClass(class)     是否有指定类名，返回 true // false
	$(this).hasClass("protected")
	$(this).is('.one')   类名是不是one。返回 true // false

### <3>  filter(expr|obj|ele|fn)     （字符串\对象\DOM元素\function函数）
筛选出与指定表达式匹配的元素集合。
这个方法用于缩小匹配的范围。用逗号分隔多个表达式

### <4>  is(expr|obj|ele|fn)
其中至少有一个元素符合要求，返回true

### <5>  map(callback)
将一组元素转换成其他数组（不论是否是元素数组）
callback：给每个元素执行的函数

	let arr=[1,2,3,4];
	    let result = arr.map(function(value,index){
	        return value*2;
	    });
	console.log(arr)        //[1,2,3,4]
	console.log(result)     //[5,6,7,8]

### <6>  has(expr|ele)    检测包含有特定子元素 
保留包含特定后代的元素，去掉那些不含有指定后代的元素。
.has()方法将会从给定的jQuery对象中重新创建一组匹配的对象。提供的选择器会一一测试原先那些对象的后代，含有匹配后代的对象将得以保留。

$('one').has('span')    检测one下包含span元素

### <7>  not(expr|ele|fn)   删掉选中的元素

### <8>  slice(start, [end])   选取一个匹配的子集
	$('li').slice(0,2).css('color','red');

### <9>  first
### <10>  last


##    查找

###  <1>  children([expr])     查找子元素
	$("div").children()   找到div所有的子元素
	$("div").children(".selected")    找div中类名为.selected的子元素

###  <2>  parent([expr])   查找指定元素的父元素
	$("p").parent()   查找p的父元素
	$("p").parent(".selected")    查找p的父元素中类名为selected的父元素。

###  <3>  parents([expr])   筛选祖先元素的表达式
	$("span").parents()   找span所有的父辈元素

###  <4>  parentsUntil([expr|element][,filter])    当前元素的所有的父辈元素，直到遇到匹配的那个元素为止。
找某个范围之内的父元素

###  <5>  offsetParent()    查找最近的具有定位属性的父元素
   
###  <6> next([expr])
	$("p").next()   找紧邻p的元素  同级

###  <7> nextAll([expr])
###  <8> nextUntil([exp|ele][,fil])

###  <9> find(expr|obj|ele)   找他里面的子元素
	$("p").find("span")
	与$("p span")相同。

###  <10>  closest(expr|object|element)     从元素本身开始，逐级向上级元素匹配，并返回最先匹配的元素。
返回0或1个元素。若本身符合，返回本身。
	li.closest('div')    找li最近的一个div（从父辈中找）
	li.closest('p')    找p，若没有，就找不到
*	事件委派

###  <11>  prev([expr])
	$("p").prev()    p前边的一个元素

###  <12>  prevAll([expr])
查找当前元素之前所有的同辈元素

###  <13>  prevUntil([exp|ele][,fil])

###  <14>   $("div").siblings()   找同辈元素
找到每个div的所有同辈元素。      同级当中 除div以外的其他元素
	$("div").siblings().slideup();   收起来
	$("div").siblings().slidedown();   放下
	$("div").siblings().slidetoggle();   与之前状态相反



##	串联

###  <1>  add(expr|ele|html|obj[,con])               ？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？
把与表达式匹配的元素添加到jQuery对象中。这个函数可以用于连接分别与两个表达式匹配的元素结果集。
	$('li').add('p').css('color','blue');		// 串联属性
原来只选的 li ，对li操作，add后，把li 和 p 一起操作
	
###  <2>  andSelf()   已删

###  <3>  addBack()	 添加堆栈中元素集合到当前集合，一个选择性的过滤选择器  ？？？？？？？？？？？？？？？？？？？？？？？
$('ul').ep(0).next().addBack().css('color','blue')
	原来只操作ep(1)，加addBack()之后，ep(0)和ep(1)一起操作，把之前的那个也选上。

###  <4>  contents()  查找匹配元素内部所有的子节点（包括文本节点）。 子元素
相当于   childNodes

###  <5>  end()   回到最近的一个"破坏性"操作之前。即，将匹配的元素列表变为前一次的状态。
*	"破坏性"操作:
	'add', 'andSelf', 'children', 'filter', 'find', 'map', 'next', 'nextAll', 'not', 'parent', 'parents', 'prev', 'prevAll', 'siblings' and 'slice'


##   事件

###  <0>  ready(fn)
在DOM加载完成时运行的代码，可以这样写：
	$(document).ready(function(){
	  // 在这里写你的代码...

###  <1> button.on('click mouselave',function(){   //事件委派
        box.slideToggle();
    })

$('box').on('click','li',function(){   //事件委派
    $(this).css('background','red');
})

###  <2>  button.off();//干掉所有事件
    button.off('click');//移除掉点击事件
    
###  <3> bind  添加   不支持事件委派    为每个匹配元素的特定事件绑定事件处理函数。
    unbind  删    不支持事件委派
点p时，弹出1
	$("p").bind("click", function(){
	  alert( 1);
	});

###  <4> one     为每一个匹配元素的特定事件（像click）绑定一个一次性的事件处理函数

在每个对象上，这个事件处理函数只会被执行一次。
	$("p").one("click", function(){      、、当所有段落被第一次点击的时候，显示所有其文本。
	  alert( $(this).text() );
	});

###  <4>  trigger（）   自动检测到的时候自动触发   集合
###  <5>  triggerHandler   
*    li.trigger('click')  所有的li都会执行触发    有浏览器默认行为
*    li.triggerHandler('click')  只有第一个li会触发('click')   没有浏览器默认行为

###  <6> button.hover(function(){    //事件切换
        $(this).css('background','red');
    },function(){
        $(this).css('background','blue');
    })

##   事件
blur([[data],fn])
change([[data],fn])
click([[data],fn])
dblclick([[data],fn])
error([[data],fn])
focus([[data],fn])
focusin([data],fn)
focusout([data],fn)
keydown([[data],fn])
keypress([[data],fn])
keyup([[data],fn])
mousedown([[data],fn])
mouseenter([[data],fn])
mouseleave([[data],fn])
mousemove([[data],fn])
mouseout([[data],fn])
mouseover([[data],fn])
mouseup([[data],fn])
resize([[data],fn])    当调整浏览器窗口的大小时，发生 resize 事件。
	$(window).resize(function(){
	  alert("Stop it!");
	});
scroll([[data],fn])
select([[data],fn])    
	当 textarea 或文本类型的 input 元素中的文本被选择时，会发生 select 事件。
submit([[data],fn])
	当提交表单时，会发生 submit 事件。     该事件只适用于表单元素。

unload([[data],fn])
	在当用户离开页面时，会发生 unload 事件。



###  <>	  index()       搜索匹配的元素，并返回相应元素的索引值，从0开始计数。
$(this).index();  //当前它的下标
 
has返回的是不是bull值？

$(this)  打包成JQuery
$() 中可以传（函数  选择器  原生的JQuery/html对象）


$('.one')  是对象
$('.one')  
$('.one')  
是不同的对象

###  <> 
###  <> ??????????????????????????????????????????????????
###  <> 


## 属性 ##

attr和prop的区别：
attr  -->   attribute   set get    操作自定义属性
prop  -->   porptype    obj.       操作标准属性

###  <1>  attr(name|properties|key,value|fn)   操作自定义属性
设置或返回被选元素的属性值。

###  <2>  prop(name|properties|key,value|fn)   操作标准属性
获取时： 获取它的第一个元素的属性值    获取第一个
设置时： 设置这类所有的元素属性值      设置全部

*	返回属性的值：
	$(selector).prop(property)
*	设置属性和值：
	$(selector).prop(property,value)
*	使用函数设置属性和值：
	$(selector).prop(property,function(index,currentvalue))
*	设置多个属性和值：
	$(selector).prop({property:value, property:value,...})

let nowsrc = $(this).find('img').prop('src');   获取这个的src
picimg.prop('src',nowsrc);                      设置src

###  <3>  removeAttr(name)     删除img的name属性
$("img").removeAttr("src");
###  <4>  removeProp(name)



##  CSS 类 

###  <1> addClass(class|fn)
$("p").addClass("selected");
	box.addClass(function(index,value){
      return value + 'one'; //最后输出 class='box boxone'
	})

###  <2> removeClass([class|fn])
###  <3> toggleClass(class|fn[,sw])
  如果存在   --> 删除
  如果不存在 --> 添加



##  HTML代码/文本/值   ?????????????????????????????????????????

###  <1>  html([val|fn])
###  <2>  text([val|fn])
###  <3>  val([val|fn|arr])



##   效果 

基本
###  <1>  show([speed,[easing],[fn]])
speed:slow,normal,fast    1000 毫秒
easing:  默认'swing'   linear
function(){}

###  <2>  hide([s,[e],[fn]])
###  <3>  toggle([s],[e],[fn])


滑动
###  <1>  slideDown([s],[e],[fn])   ???????????????????????????????????????????????????????
只调整元素的高度
###  <2>  slideUp([s,[e],[fn]])
###  <3>  slideToggle([s],[e],[fn])


淡入淡出
###  <1>  fadeIn([s],[e],[fn])
###  <2>  fadeOut([s],[e],[fn])
###  <3>  fadeTo([[s],o,[e],[fn]])
opacity：一个0至1之间表示透明度的数字。
###  <4>  fadeToggle([s,[e],[fn]])


自定义
###  <1>  animate(p,[s],[e],[fn])
box.animate({left:'300',width:'+=400'})

###  <2>  stop([c],[j])
clearQueue:如果设置成true，则清空队列。可以立即结束动画。
gotoEnd:让当前正在执行的动画立即完成，并且重设show和hide的原始样式，调用回调函数等。
.stop();
	begin.click(function(){
        box.animate({width:'+=50',left:'+=300'},'slow').animate({top:'+=300'},'slow')
    })
    stop.click(function(){
        box.stop()
	//	box.stop(true,true)
    })

###  <3>  delay(d,[q])
duration:延时时间，单位：毫秒
queueName:队列名词，默认是Fx，动画队列。

###  <4>  finish([queue])
停止当前正在运行的动画，删除所有排队的动画，并完成匹配元素所有的动画。



设置
###  <1>  jQuery.fx.off
开启页面内的动画
###  <2>  jQuery.fx.interval
设置动画的帧率




##   CSS

CSS
###  <>   css(name|pro|[,val|fn])
###  <>   jQuery.cssHooks


位置
###  <1>   offset([coordinates])    在当前视口的相对偏移
	var offset = p.offset();
	p.html( "left: " + offset.left + ", top: " + offset.top );

###  <2>   position()    获取位置，只获取


###  <3>   scrollTop([val])
元素相对滚动条顶部的偏移。
###  <4>   scrollLeft([val])


尺寸
###  <1>   height([val|fn])  获取元素当前计算的高度值（px）。
###  <2>   width([val|fn])    box的宽 width
	$("p").height();       获取高    获取第一个
	$("p").height(20);     设置高    设置所有的高

###  <3>   innerHeight()    box的宽 width + padding
###  <4>   innerWidth()
获取第一个匹配元素内部区域高度（包括补白、不包括边框）。

###  <5>   outerHeight([soptions])
###  <6>   outerWidth([options])      width + padding + border
第一个匹配元素外部高度（默认包括补白和边框）。

box.width()           //300  box的宽 width
box.innerWidth()      //316  box的宽 width + padding
box.outerWidth()      //326  box的宽 width + padding + border值 
box.outerWidth(true)  //426  box的宽 width + padding + border + margin



文档处理

内部插入  -->   子元素
###  <1>   append(content|fn)   主动往父元素中插入一个子元素     父元素.append(子元素)
	let span = $('<span>').html('我是span')
    box.append(span)
    $('.box').append('<span>直接创建span</span>').css('')  css操作的是box.前边的
    $('.box').append(function(index,value){
        return `<p>函数创建的p</p>`
    })
###  <2>   appendTo(content)
子元素.appendTo(父元素).css('')    css操作的是 子元素 前边的             
###  <3>   prepend(content|fn)     用法同上
$('.box').prepend('<span>插入到最前面</span>')
###  <4>   prependTo(content)


外部插入
###  <1>   after(content|fn)   在每个匹配的元素之后插入内容。
###  <2>   before(content|fn)   在每个匹配的元素之前插入内容
box.after($('<h1>插入到后面</h1>'))
box.before($('<h1>插入到前面</h1>'))

###  <3>   insertAfter(content)   顺序和上面的相反
###  <4>   insertBefore(content)
$('<h1>插入到前面</h1>').insertBefore(box)
$('<h1>插入到后面</h1>').insertAfter(box)



包裹
###  <1>   wrap(html|ele|fn)      
给每个p标签外包一个 div .box
$('p').wrap('.box')    

###  <2>   unwrap()
$('p').unwrap   拆包

###  <3>   wrapAll(html|ele)
将所有匹配的元素用单个元素包裹起来
$('p').wrapAll('<div>')

###  <4>   wrapInner(html|ele|fn)
$('p').wrapInner('<p>')




替换
###  <1>replaceWith(content|fn)
$('p').replaceWith('<span>替换后的内容</span>')
$('p').replaceWith('box')
$('p').replaceWith($('.box'))

###  <2>replaceAll(selector)
$('.box').replaceAll($('p'))    box被p标签替换



删除
###  <>   empty()   删除子元素
	$("p").empty();   清空p中所有的子元素

###  <>   remove([expr])   删除自己本身
	$("p").remove();   删除p标签    把自己删除
不会把匹配的元素从jQuery对象中删除，因而可以在将来再使用这些匹配的元素。但除了这个元素本身得以保留之外，其他的比如绑定的事件，附加的数据等都会被移除。
###  <>   detach([expr])
	$("p").detach();  删除p标签    把自己删除
这个方法不会把匹配的元素从jQuery对象中删除，因而可以在将来再使用这些匹配的元素。与remove()不同的是，所有绑定的事件、附加的数据等都会保留下来。


从页面中删除，
区别：把他原有的事件、属性保存下来


复制
###  <>  clone([Even[,deepEven]])
会把子元素一起克隆过来

lis.clone()     可以把子元素一起复制过来
lis.clone(true)     true会把子元素、数据、事件一起克隆过来
把事件一起复制

	let clone = lis.clone();
    $('ol').append(clone)

拷贝  值 的是 “ 深拷贝 ”



###  <>   queue
###  <>   dequeue
//    定义的队列名字。
    $(document).queue('myqueue',aa)
    $(document).delay(2000,'myqueue').queue('myqueue',bb)
    $(document).dequeue('myqueue')

###  <>  
###  <>  
###  <>  
###  <>  $(document).queue

 







###  <>   $('div',box)  ??????????????????????????????????????


###  <> box.slideToggle();
###  <> box.slideUp;








###  <>   加下标编程原生对象
 	$('button');
    let mask = $('.mask')[0];
###  <>   不加下标，是JQuery


 $(this).find(img)[0].src;

 




``` 























