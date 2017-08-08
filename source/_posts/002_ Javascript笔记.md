
---
title: 002_JavaScript笔记
---
 
## JavaScript-02

```bash
####★技巧★    JS 引入   返回 从哪来到哪去
<script src="javascript:history.go(-1)">返回</script>
<a href="javascript:history.go(-1)"></a>


####★技巧★    a.toExponential(3)
科学计数法
num = num.toExponential(3)
   "3.333e+0"

####★技巧★		num.toFixed(2);
限制小数点后两位  num = num.toFixed(2);


####★技巧★   注意filder中筛选 返回的是条件 ：  ‘==’  双等于
let r = choicelist.filter(function (v, i) {
    return v.id == o.id
});

####★技巧★   find  eq(this.index())    查找 li下边的 类名为 '.num img' 的标签
picEl = $(this).closest('li').find('.num img').attr('src');

$(this).removeClass('active').eq($(this).index()).addClass('active')


####★技巧★   javescript:void(0)
<a href="javescript:void(0)">删除</a>

####★技巧★  计算数组内值的和

let arr = [1,2,3,4,5,6,'7'];
let sums = arr.reduce(function (a, b) {
    return Number(a) + Number(b);
});
console.log(sums)
	28



####★技巧★		target与currentTarget的区别？ 

通俗易懂的说法： 
比如说现在有A和B， 
A.addChild(B) 
A监听鼠标点击事件 
那么当点击B时，target是B，currentTarget是A 
也就是说，currentTarget始终是监听事件者，而target是事件的真正发出者 

target在事件流的目标阶段；currentTarget在事件流的捕获，目标及冒泡阶段。

target指向被单击的对象而currentTarget指向当前事件活动的对象（一般为父级）。 


####★技巧★ 
alert() 显示带有一段消息和一个确认按钮的警告框。
confirm() 显示带有一段消息以及确认按钮和取消按钮的对话框。
prompt() 显示可提示用户输入的对话框。
close() 关闭浏览器窗口。
open(url,name,feafurse,replace) 通过脚本打开新的窗口URL要在新窗口中显示的文档的 URL。如果省略了这个参数,那么新窗口就不会显示任何文档

	var input=prompt('输入',' ');  //都是字符串
	var flag=confirm(123); 
	open('error.html','_blank','width=500,height=500,left=200,top=100');
	open('error.html','_self','width=500,height=500,left=200,top=100');

####★技巧★ ES6有哪些新的？
	  .ES6的新特性:箭头操作符=>，模板字符串(`${asd}`)等等
####★技巧★  JSON.parse      /字符串转化成对象 数组
     JSON.stringify   对象转换为一个JSON字符串

####★技巧★  format   讲任意类型转换成字符串
a = format(123)
####★技巧★ * 
.a{
	opacity: 0;
	transition: all 1s;
}
.a:hover{
	opacity: 1;
}

鼠标移动过去过1秒显示
####★技巧★  获取元素的宽度，高度
	window.onload=function(){
		let box1=document.getElementsByClassName('box');
		console.log(getComputedStyle(box[0],null).width);
		console.log(getComputedStyle(box[0],null).height);
			//可以获取所有，但只能获取，不能设置
	}
####★技巧★ 
canvas 画的图出现不停复制，清空不了情况。给border加一个边框

####★技巧★    cursor
cursor：move	   此光标指示某对象可被移动。

####★技巧★		弹幕  
`<marquee>弹幕标签</marquee>`
<marquee>弹幕标签</marquee>

####★技巧★    面向对象   选取颜色   设置
*	HTML：
	<input type="color" class="miaocolor" value="#000">

*	JS:
	miaocolor.onchange=function(){            //描边颜色
        palette.strokeStyle=this.value;
    };
    tiancolor.onchange=function(){            //填充颜色
        palette.fillStyle=this.value;
    };
	miaobtn.onclick=function(){           //描边
        palette.type = 'stroke';
    };
    tianbtn.onclick=function(){           //填充
        palette.type = 'fill';
    };

*	function Palette(obj,mask,ctx){
		this.type = 'stroke';
		this.fillStyle = '#000';
	    this.strokeStyle = '#000';
	}

*	Palette.prototype={
	    //初始化
	    init:function(){
	        this.ctx.lineWidth = this.lineWidth;
	        this.ctx.strokeStyle = this.strokeStyle;     //OK
	        this.ctx.fillStyle = this.fillStyle;        //OK
	        this.ctx.lineCap = this.lineCap;
	        // this.ctx[type]();
	        // self[type]();
	    },
	}


//选择 填充、描边类型
self.ctx[self.type]();




####★技巧★  选择  输入
var colorchoose=document.querySelector("input[type=color]");
var widthchoose=document.querySelector(".linewidth input[type=number]");

####★技巧★   浏览器   ！！！警告！！！！
	颜色应该是：#000000   
The specified value "#000" does not conform to the required format.  The format is "#rrggbb" where rr, gg, bb are two-digit hexadecimal numbers.

####★技巧★   浏览器   ！！！报错！！！！
Uncaught SyntaxError: Unexpected token :

可能是上面函数少了一个 {  }

####★技巧★   浏览器   ！！！报错！！！！
index.js:16 Uncaught TypeError: Cannot read property 'getContext' of null   at index.js:16

把相关的script引用句放在html最下边

JS中写：		window.onload=function(){}

####★技巧★   label   表单元素
	当用户选择该标签时，浏览器就会自动将焦点转到和标签相关的表单控件上。
####★技巧★  注意 鼠标点击嵌套  内层也要写 function(e)   eeeeeee
	canvas.onmousedown=function(e){
        canvas.onmousemove=function(***e***){
        }
	}
####★技巧★  Math.pow
Math.pow

####★技巧★   弧度  角度转换 
*	弧度=（π/180）×角度     
*	角度=180/π×弧度
####★技巧★
如果某个事件报错  看看是否能获取到那个元素

####★技巧★    CSS设置全屏
 html:-webkit-full-screen{
            background: yellow;
        }

####★技巧★	全屏
	quanping:function(){
        if(document.documentElement.requestFullscreen){
            document.documentElement.requestFullscrren();
        }else if(document.documentElement.webkitRequestFullscreen){
            document.documentElement.webkitRequestFullscreen();
        }else if(document.documentElement.mozRequestFullscreen){
            document.documentElement.mozRequestFullscreen();
        }
    }

###   全屏 ，退出全屏
// Webkit (works in Safari5.1 and Chrome 15)
element.webkitRequestFullScreen();
document.webkitCancelFullScreen();
 
// Firefox 10+
element.mozRequestFullScreen();
document.mozCancelFullScreen();
 
// W3C 提议
element.requestFullscreen();
document.exitFullscreen();


####★技巧★   属性选择器
let done=document.querySelector('input[type=text]');

####★技巧★   清空内容  ！！''中不能有空格！！！
table.innerHTML=''; //清空内容   ！！ ''中不能有空格！！！

####★技巧★    立即获取焦点
input.focus();//立即获取焦点

####★技巧★
*	element.getAttribute(attributename)
`attributename	字符串值。	必需。需要获得属性值的属性名称。`

####★技巧★   分割   split函数 括号中要 （'; '） 在逗号后边留一个空格    （=） 等号不加空格
	let arr=cookie.split('; ');  

####★技巧★   some中 是  == 双等号
	let a=this.currentele.some(function(value,index,obj){
		return value.innerText==text;
	})

####★技巧★   注意循环  输出false会坏事   循环只是等 true,输出的false会打乱结构，干扰结果  
	for(let i=0;i<this.currentele.length;i++){
		if(this.currentele[i].innerText==text){
			return true;
		}/*else{
			// console.log('不相等')
			continue aa;
			return false;
			// alert(1)
		};*/
	}
####★技巧★   绑定this  把外边的this传到函数当中
document.body.onkeydown=function(e){}.bind(this); //绑定this  把外边的this传到函数当中


####★技巧★		数值转换字符串
=String.fromCharCode(Math.floor(Math.random()*26)+65);
####★技巧★   定义元素样式
	ele.style.cssText=`
		width: 50px;
		height: 50px;
		line-height: 50px;
		background: #F2F2F2;
		text-align: center;
		position:absolute;
		left:${lefts}px;
		top:${tops}px;
		`
####★技巧★   动画结束之后
	tr.addEventListener('webkitTransitionEnd',function(){
					tr.removeChild(obj.parentNode);
####★技巧★   /*	let student[1,2,{},4]   forEach的是student的值，也就是value：1,2,{},4      {} 内为对象，obj.name   对象.属性*/
	let student=[
			{'name':'任雨','age':'18','sex':'女','loca':'山西','tel':12345678},
			{'name':'曹越','age':'19','sex':'男','loca':'山西','tel':87543213},
			{'name':'李虎','age':'16','sex':'女','loca':'山西','tel':87654456},
			{'name':'刘婷','age':'18','sex':'男','loca':'山西','tel':09876542}
		]

	
####★技巧★   ${}  花括号  输入内容
let tr=$('<tr>');   此处tr是标签
tr.innerHTML= `<td> ${obj.name} </td>`    
####★技巧★   注意   innerHTML 大写   
tr.innerHTML    tr.innerHtml--》 错误
####★技巧★   
let oldv=div.innerText; //获取标签内的文字内容
input.value=oldv;    //value是input的属性，obj没有value这个属性


####★技巧★   给box中插入 son
	for(let i=0;i<100;i++){
		box.innerHTML += `<div class='son'></div>`;
	}

####★技巧★  给随机颜色
	obj.style.background='rgb('+Math.floor(Math.random()*256)+','+Math.floor(Math.random()*256)+','+Math.floor(Math.random()*256)+')';

####★技巧★   nodeName   后面要大写
if(obj.nodeName=='P'){
node.name  
####★技巧★   输入文本框
`<textarea name="" id="" cols="30" rows="10" maxlength="100" >输入文本</textarea>`
####★技巧★   没有报错  没有现象
*	检查元素的下标
	`let btn=$('button')[0];`



####★技巧★  输入文本
	<div class="box" contenteditable="true">
		输入文本
	</div>
	<textarea name="" id="" cols="30" rows="10">
		输入文本
	</textarea>

####★技巧★		兼容问题
	//IE高版本   兼容问题
	div.addEventListener('click', function(){alert(1)}, false)

	//IE低版本   兼容问题
	div.attachEvent('onclick', function(){alert(1)})
*	this 是指向其他地方
####★技巧★
box.style.cssText='';

####★技巧★
this.######
let aa=this;

function(){
	aa.
}

####★技巧★
在第一个前面插入
imgbox.insertBefore(last,first);

####★技巧★  报错   setTimeout is not defined
把这一行重新写

####★技巧★		！！！报错！！！
语法错误    下标越界   下标没写

box1[0].style.borderRadius='50%';
box1[0].style['border-radius']='50%';

box1[0].style.fontSize='50%';
box1[0].style.['font-size']='50%';

####★技巧★			！！！报错！！！
Uncaught TypeError: Cannot read property 'style' of undefined
at HTMLDivElement.caoyue1.(anonymous function).onclick 

*	注意事件下标越界：caoyue1[5].style.background='red';	下标只有 0--4 

####★技巧★		！！！报错！！！
*	Uncaught TypeError: Cannot set property 'innerText' of null
script里操作了body的东西。script在body前面。
解决方法：把script内容写进body中，或写在最后。</html>之后。

####★技巧★
	浏览器报错：  因为while() 括号不完整。少半个 ）   
	或是（）的地方写成了 {}
	Uncaught SyntaxError: Unexpected token {

####★技巧★
F12 在浏览器打开
Alt + table 切换窗口

####★技巧★	  这三个不用加下标
*	let box=document.querySelector('.box');
*	let box=document.querySelectorAll('.box');
*	let win3=document.
*	
*	getElementBy
*	
*	
*	()
####★技巧★
自动轮播的时间要比切换的时间多点儿


####★技巧★
	获取的方法：
*	let win1=document.querySelector('.win');
*	let img2=document.querySelectorAll('.imgbox li');
*	let win3=document.getElementById()
*	let win4=document.getElementsByClassName()
*	let win5=document.getElementsByTagName()
*	let win6=document.getElementsByName()
####★技巧★
按住空格多选，同时操作

####★技巧★
*	let imgbox=document.querySelector('.imgbox');
*	let imgs=document.querySelectorAll('.imgbox li');
####★技巧★
animate.js的调用

####★技巧★
继承  把一个对象的方法冒充给另一个对象
		冒充法
callback.call(obj);

传函数
this.aa=function();
zhangsan.aa.call(lisi); 

传函数传参
this.aa=function(a,b);
zhangsan.aa.call(lisi,12,32);
zhangsan.aa.call(lisi,[10,20]);  

####★技巧★
注意传参  width 是‘width’
animate(box,'width',500)
####★技巧★
屏蔽a标签的默认行为  ？？？？？？？？？？？？？？？？？？？
？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？
*	`<a href="javascript:;"></a>`
*	`<a href="#"></a>`
*	`<a href="http://www.baidu.com" onclick=" return false; ">  Click Me  </a>`

####★技巧★	
	btn.play=function(){
		this.play=aa;
		添加自定义属性，方法
	}
	for(let i=0;i<5;i++){
		btn[i].aa=i;
		btn[i].onmouseout=function(){
			btn[i].style.background='none';
			this.style.background='none';
			box[this.aa].style.background='none';
		}
	}

####★技巧★	
	input1[i].onmouseover=function(){
		// this.style.background='red';	等同于下一句
		input1[i].style.background='red';
		kw[i].style.height='200px';
		let a=this;
		function aa(){
			input1[i].style.background='red';
			// this.style.background='red';
			这儿的this需要上边 let =this 一下，否则不能用。
		}
	}

####★技巧★	
	for(var i=0;i<5;i++){
		input1[i].onmouseover=function(){
			input1[i].style.background='red';
			kw[i].style.height='200px';
		}
	}
	for(let i=0;i<5;i++){
		input1[i].onmouseover=function(){
			input1[i].style.background='red';
			kw[i].style.height='200px';
		}
	}
*	var 执行完以后，i在循环外边可以访问。let不行。
*	let循环时，可以保存每个I的值，var不行。


####★技巧★	
.hidden{
	display: hidden;
}
.show{
	display: show;
}
box1[0].className = 'box show';
box1[0].className = 'box hidden';

####★技巧★	
box1[0].id='color';		添加id
box1[0].className = 'box color';	添加类名=‘原有类名  新类名’

####★技巧★
清除浮动：
<div style='clear:both'></div>
####★技巧★
location
####★技巧★
filter


####★技巧★
*	把函数写进文本中
>	document.body.innerText=(day+'天'+hour+'小时'+min+'分'+second+'秒');

####★技巧★  ???????????????????????????????????
	/*if(!(arr instanceof Array)){
		return ;
	}
	???????????????????????????????????
	if(!Array.isArray(arr)){
		return ;
	}*/
####★技巧★
	数组的遍历+判断
	let flag=arr1.some(function(value,index,arr){
		return console.log(value,index,arr)
	})

	some(function(值   下标   遍历的数组){})	回调函数
	返回值：	布尔值。如果数组中有元素满足条件返回 true，否则返回 false。
	
	every(function(值   下标   遍历的数组){})
	返回值：	布尔值。如果所有元素都通过检测返回 true，否则返回 false。
	
	var arr=[3,-1,1,6,12,-1,65,1,-4];
	var flag=arr.some(function(value,index,arr){
		return value>0;
	})
	document.write(flag);

####★技巧★
	遍历属性(遍历数组下标)		
for(let i in arr)
	var arr=[3,-1,1,6,12,-1,65,1,-4];
	document.write(arr+'<br>');
	for(let i in arr){
	console.log(i+'--'+arr[i]);
}
		
	遍历属性值(遍历数组元素)		
for(let i of arr)
for(let i of arr){
	console.log(i);
}

####★技巧★
function huoqu(arr,num=3){}  函数中num给一个默认值3。调用的时候传参就可以不用传。


####★技巧★
	对象元素的顺序：自己构造---自己原型--父构造---父原型

####★技巧★
构造函数和普通函数差不多

####★技巧★
查看浏览器 继承对象的方法，在浏览器console中输入console.dir(String)
console.dir(String)

####★技巧★
`true 和  false 不能进行  true++  true-- 运算`

####★技巧★
注意创建对象的JSON方式的逗号
####★技巧★  instanceof 判断
	console.log(str instanceof String);    //false
	instanceof  只能判断数组和对象，不能用来判断字符串和数字等.
	console.log(str instanceof arrAy)
	console.log(str instanceof Object)
	
####★技巧★  判断是否为字符串
	if(typeof(str1)!='string'){
		return '不是字符串';
	}
####★技巧★  注意分割空格（' '）中间要有空格
let arr=str.split(' ');
#####
	无聊望见了犹豫(磨料望跟六摇椅)          
	达到理想不太易(达到类桑霸台仪)
	即使有信心(即西要森森)                  
	斗志靠抑止(导既靠译既)
	
	谁人定我去和留(岁人顶我会望老)          
	定我心中的宇宙(顶我僧中的与奏) 
	只想靠两手向理想挥手 (只想靠浪扫 航类桑非扫) 
	
	问句天几高心中志比天更高(问归听给沟僧钟执笔天更高)
	自信打不死的心态活到老 (自森大霸四（sei1）的僧台乎到楼) 
	OH… 我有我心底故事 (喔嗷嗷...摸幽默僧得古四（sei1）) 
	亲手写上每段得失乐与悲与梦遗 (岑搜噻上母得（dei4）当撒浪于被与梦遗) 
	OH… 纵有创伤不退避 (喔嗷嗷... 总要从桑把腿被) 
	梦想有日达成找到心底梦想的世界 (梦桑幽雅大事遭斗僧得梦桑的四该~)          
	终可见... （总豪给...）
	
	谁人没试过犹豫 （水人毛四（sei2）国药仪）     
	达到理想不太易(达到类桑霸台仪) 
	即使有信心  (即西要森森)                      
	斗志却抑止 (导既靠译既)
	谁人定我去和留  (岁人顶我会望老)              
	定我心中的宇宙 (顶我僧中的与奏) 
	只想靠两手向理想挥手 (只想靠浪扫 航类桑非扫)   
	问句天几高心中志比天更高 (问归听给沟僧钟执笔天更高)
	自信打不死的心态活到老 (自森大霸四（sei）的僧台乎到楼)
	OH… 我有我心底故事 (喔嗷嗷...摸幽默僧得古事（sei1）) 
	亲手写上每段得失乐与悲与梦遗 (岑搜噻上母得（dei4）当撒浪于被与梦遗) 
	OH… 纵有创伤不退避  (喔嗷嗷... 总要从桑把腿被)
	梦想有日达成找到心底梦想的世界  (梦桑幽雅大事（sei4）
	遭斗僧得（dei4）梦桑的四（sei4）该~)
	终可见... （总豪给...）
	
	
	







##★★★★★★★★★★★★对象简写★★★★★20170425★★★★★★★★★★★★★
//#####	对象简写
	允许变量名作为对象的属性名,变量的值对应对象的属性值
		let age=20;
		let sex='boy';
		let zhangsan={age,sex};
		等价于:
		let lisi={age:18,'sex':'nv',tall:180};

##### 对象属性允许是表达式
	let firstname='hello';
		let lisi={
			['a'+'ge']:18,
			[firstname]:'li',  //等价于：hello:'li' 
		//	hello:'li'
		}
		console.dir(lisi);
*	此方法不允许嵌套


	ren.prototype={	}  //原型对象

#####  一个对象指向另一个对象   继承        class student extends person{ super(); }
		//一个对象指向另一个对象
		class person{
			constructor(){
				this.name='zhangsan';
				this.age=18;
			}
			play(){
				alert(1);
			}
		}
		var zhangsan=new person();
		//继承  指向             student可以调用person的属性、方法
		class student extends person{
			constructor(){
				super();
				this.classes='wuif1702';
				this.num=1702;
			}
			homework(){
				alert('写作业');
			}
		}
		var lisi =new student();
		document.write(lisi.name);
		console.log(lisi.age);
		console.log(lisi.num);

*	继承方法二：
	`var students.prototype=new person();`  //原型对象






# ★★★★★★★★★★★★字符串对象★★20170425★★★★★★★★★★★★★★★★
	var arr=[1,2,3,4],arr1=new Array(1,2,3,4);
	var str='abcd';
	等价于：
	var str1=new String("abcd");
	
	
####	1.内置对象
			Global 全局
			Object
			String
			Array
			Number
			Math	数学方法对象
			Boolean
			Function
			RegExp	正则
		2.数组对象
			DOM
			BOM

#### 一\属性
		1.length		不识别空字符、不区分中英文
		计算字符串的长度
		2.constructor
		对象的构造函数
			console.log(str.length);		//返回长度
			console.log(str.constructor);	//返回构造函数

#### 二\ 方法
		获取类型:
		1.myString.charAt(num)
			返回在指定位置的字符.
		2.myString.charCodeAt(num)
			返回指定位置的字符的unicode编码
		3.String.fromCharCode()
			接受一个或多个自定的unicode值,然后返回一个或多个字符串
				console.log(str.charAt(0));		//返回指定位置字符。下标从0开始
				console.log(str.charAt(3));		
				console.log(str.charAt(5));     //-1和5为空
				console.log(str.charAt(-1));
				console.log(str.charCodeAt(1));	//返回指定位置字符对应的unicode编码
				console.log(String.fromCharCode(97));//将unicode编码转换为响应字符

#### 查找类型	
		1.myString.indexOf("")
		    返回某个指定的字符串,在字符串中首次出现的位置
		    如果要检索的字符串值没有出现，则该方法返回 -1。
		2.myString.lastlndexOf()
			返回指定的字符串值最后出现的位置
		3.myString.match()
			3.1  console.log(str.includes("d"));  //返回 true false
			在字符串中检索指定的值,返回的值就是指定的值
		4.search()
			只能作用于正则
		5.myString.replace()
			将字符串中的一些字符替换为另外一些字符
		6.myString.repeat(5)
			将字符串重复5次
			changdu='*'.repeat(str1.length);
				str2="asd";
				var res=str2.repeat(5);
				alert(res);

#### 截取类型
		1.myString.slice(start,end)。
			从指定的开始位置，到结束位置(不包括)的所有字符串。如果不指定结束位置，则从指定的开始位置，取到结尾
			slice参数可以是负数，如果是负数，从-1开始指的是字符串结尾。
			  eg:var str1=str.slice(-7,-3);   
		2.substring(start,end)
			和 myString.slice(start,end)的用法一样，唯一的区别是不支持负数。
		3.substr(start,length)
			从指定的位置开始取指定长度的字符串。如果没有指定长度，从指定开始的位置取到结尾。		

#### 转换类型
		1.split("分割位置i",[指定的长度n])
			将一个字符串分割成数组(分割成长度为N的数组)。从分割位置i开始转换n个。 
		2.toLowerCase();
			用于把字符串转换为小写。
		3.toUpperCase()
			将字符串转换为大写.
				console.log('abcd'.toUpperCase())
				console.log('ABcd'.toLowerCase())
#### 样式类型
		1.fontcolor()
			给字符串指定颜色，十六进制表示、red、 rgb(255,0,0)
		2.fontsize()
			指定字符串的大小 (1-7)
#### 去空     trim
	console.log(str.trim())
	console.log(str.trimLeft())
	console.log(str.trimright())

###		eg:
		//搜索 str1 中是否有 str2 .
		function isinclude(str1,str2){
			if((typeof(str1)!='string')&&(str2 instanceof String)&&(arguments.length>=2)){
				return '不是字符串';
			} else{
				if(str1.indexOf(str2)==-1){
					return false;
				}else{
					return true;
				}
			}
		}
		str1='asdd';
		str2="dd";
		var result=isinclude(str1,str2);
		alert(result);
		
		3.
		console.log(str.match("d"));
		等同于match
		3.1  console.log(str.includes("d"));  //返回 true false

###### eg：	将str中的str1全部替换为"***"
		str='abcsdsabcsdsabc';
		function rpls(str,str1){
			let changdu='';
			for(let i=0;i<str1.length;i++){
				changdu+='*';
			}
			let newstr=str;
			while(newstr.includes(str1)){
				newstr = newstr.replace(str1,changdu);
			}
			return newstr;
		}
		var str='asdfghasdfghasdgfhasd';
		var str1='a';
		var res=rpls(str,str1);
		alert(res);

####eg
	//判断一个字符串中是否包含另一个字符串
	function isinclude(str1,str2){
		if(str1.indexOf(str2)==-1){
			return false;
		}else{
			return true;
		}
	}
	str1="acdwe";
	str2="de";
	let result=isinclude(str1,str2);
	alert(result);


	//判断一串字符串 （'one   one1   one2   '）中是否有 （one） 
	//	class= 'one   one1   one2   '
		function isele(str,ele){
			let arr=str.split(' ');
			for(let i=0;i<arr.length;i++){
				if(arr[i]==ele){
					return true;
				}
			}
			return false;
		}
		var str='one3 one1 one one4';
		var res=isele(str,'one');
		console.log(res);


	/*
	输出指定字符串在字符串中的位置
	*/
	function addres(str,str1){
		if((typeof str!='string')||(typeof str1!='string')||(document.length<2)){
			return '输入错误';
		}
			let changdu='*'.repeat(str1.length);
			let newstr=str;
			var num=0;
			let arr=[];
			let i=0;
			while(newstr.includes(str1)){
				/*num=newstr.indexOf(str1);
				console.log(num);
				arr[i]=num;
				i++;*/
				arr.push(newstr.indexOf(str1));
				newstr=newstr.replace(str1,changdu);
			}
			document.write(arr+'<br>');
			document.write(newstr);
			return newstr,arr;
	}
	str="http://fanyi.youdao.com/http://fanyi.youdao.com/http://fanyi.youdao.com/http://fanyi.youdao.com/";
	str1='t';
	var add=addres(str,str1);
	console.log(add);







#####  ★★★★★★★20170425★★★★★★★★  Math  ★★★★★★★★★★★★★★★
			var num=1.998;
	//取绝对值
			var result=Math.abs(num);
		//		alert(result);
	//取整  四舍五入
			var result2=Math.round(num);
		//		alert(result2);
	//向上取整
			var result3=Math.ceil(num);
		//		alert(result3);
	//向下取整
			var result4=Math.floor(num);
		//		alert(result4);
	//最大值
			var num1=Math.max(1,2,3,43,45,6,77);
		//		alert(num1);
	//最小值
			var num1=Math.min(1,2,3,43,45,6,77);
		//		alert(num1);
	//随机数   0~1之间的随机数
			var num1=Math.random(1,2,3,43,45,6,77);
		//		alert(num1);
	//随机数   10~20之间的随机数
			var num1=Math.random(Math.random(1,2,3,43,45,6,77)*10)+10;
			
		//		alert(num1);
		//		Math.sin();
				alert(Math.PI);
				var result=Math.sin(30*Math.PI/180);
		//		alert(result);
		//		Math.cos();
		//		Math.tan();
				//保留两位小数
				var num=1.234;
				var result=num.toFixed(2);
		//		alert(result);















事件流
##★★★★★★★★★★★★  数组对象  ★★★★★20170426★★★★★★★★★★★★★
* BOM
* dom


### 遍历
//		let arr=new Array(5);
//		let arr1=Array.of(5);
//		console.log(arr);

##### 一、属性
*	1.length
	`可设置或返回数组元素的数目`
*	2.constructor
	`返回构造函数的引用`

##### 二、方法                  添加 点点点...？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？
	A.删除或添加 类
	1. myarr.push(数组元素......)		添加
		向数组的末尾添加新的元素，返回值是新数组的长度。可以一次添加多个元素
			//有...添加进去的是元素
            /*let arr3=['a','b','c','d'];
            let result=arr.push(...['a','b','c','d']);
            console.log(result)
            let result1=arr.unshift(...['a','b','c','d']);
            console.log(result1)
            let rp=arr.pop()
            console.log(rp)
            let rs=arr.shift()
            console.log(rs)*/
   *	从第2个开始截取3个元素并把字符串放进去
            // arr.splice(2,3,'a','b','c');
            // console.log(arr)
   *	 //连接符
            // let str=arr.join('-');
            // console.log(str,typeof str)
   *	//截取
            // let arr4=arr.slice(-3);
            // console.log(arr4)
   *	// 反转
            // let arr5=arr.reverse()
            // console.log(arr5)
   *	//排序
            /*let arr6=arr.sort(fn);
            function fn(a,b){
                if(a<b){
                    return -1;
                }else if(a==b){
                    return 0;
                }else if(a>b){
                    return 1;
                }
            }
            console.log(arr6)*/


	2. myarr.unshift(数组元素.....)		从开头添加
		向数组的开头加入新的元素，返回值是新数组的长度。可以一次添加多个元素
	3. myarr.pop()      	从后边删。
		删除数组的最后一个元素，返回删除的元素
	4. myarr.shift()		从前边删
		删除数组的第一个元素，返回删除的元素
		
	5.万能的添加删除函数(用于插入、删除或替换数组的元素。)
	myarr.splice(index,数量,添加的元素.....)
		(1)index 从何处开始添加或删除，必须是数值类型(数组的下标)
		(2)数量 规定了删除的个数，如果是0，则不删除
		(3)需要添加的元素，可以当作替换的元素
		(4)如果从arrayObject中删除了元素，则返回的是含有被删除的元素的数组。
	eg:		var arr=[1,2,3,4,5];
			let res=arr.push('a','v','d');
			arr.splice(1,2) //从第1个位置删掉2个。
			arr.splice(1,0,'ac','dc')//从第1个位置添加  'ac','dc'
			arr.splice(1,2,'acd','qwe','dsa');//从第一个位置删除2个，再添加  'acd','qwe','dsa'

##### B.数组的转换
*	mystr.split() //字符串分割为数组
*	myarr.join([分隔符])
	把数组元素按照指定分隔符组合成一个字符串，如果没有指定分隔符，默认是用“,”返回结果就是组合成的字符串
？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？
//		let str=arr.join('-');
//		join这一块

	let	arr=[1,2,3,4,5];
	arr.reverse(arr);     //数组反转过来

			//	数组转化为字符串
				var arr=[1,2,3,55];
//				var str=arr.join('*');
//				document.write(str)
			


##### C.数组的分割			同字符串分割
	myarr.slice()
	 从截取指定的开始位置，到结束位置(不包括)的元素。如果不指定结束位置，则从指定的开始位置，取到结尾(数组的下标)支持负数(-1开头) 返回新数组。

		数组的分割
		var newarr=arr.slice(1,3);
		document.write(arr);
		document.write(newarr);		//新数组

##### D.数组的连接
	myarr.concat()
	连接两个或更多的数组，并返回新数组，但是对原数组没有任何影响。
//		let con=arr.concat(arr1);		
//		let con=arr.concat('a','v','d');
//		let con=arr.concat(...arr1);
//		let con=arr.concat(...arr1,['zhangsan','lisi']); //可以连接多个数组
			//	拼接
			/*var arr2=[4,5,6];
			var newarr=arr.concat(arr2);
			document.write(newarr);//新数组*/

##### E.数组排序
	myarr.sort(fun) 用于对数组的元素进行排序
	1. 默认是按照字符编码的顺序进行排
	2. 如果要实现其他排序则要传入一个参数，这个参数必须要函数，并且这个函数要有两个参数
	• 若 a 小于 b，在排序后的数组中 a 应该出现在 b 之
	前，则返回一个小于 0 的值。
	• 若 a 等于 b，则返回 0。
	• 若 a 大于 b，则返回一个大于 0 的值。

	
	let	arr=[1,2,3,4,5];
	arr.reverse(arr);     	//将数组前后反转过来

	let	arr=[21,3,34,65,3,12,23,123,2];
	arr.sort(arr);   		//当做字符串比较来排序
	console.log(arr);

	排序：
	let	arr=[21,3,34,65,3,12,23,123,2];
	let arr2=arr.sort(fn); 
	function fn(a,b){     //升序
		if(a<b){
			return -1;
		}else if(a==b){
			return 0;
		}else if(a>b){
			return 1;
		}
	}
	console.log(arr2);
	/*function fn(a,b){     //降序
		if(a<b){
			return 1;
		}else if(a==b){
			return 0;
		}else if(a>b){
			return -1;
		}
	}*/

/*
 	1.判断是否存在  >0  或  <0  的数
 	2.判断数组是否都    >0  或  <0   的数
 	3.筛选 数组元素>0 的元素
 	4.删除重复的元素
 	5.从数组中随机获取任意元素
 	6.从数组中随机获取任意一个不重复的元素
*/


### eg  例子：
	// 1  判断是否存在  >0  或  <0  的数
	/*var arr=[-3,-1,0,6,12,65,1,-4];
	function cunzai(arr,num=1){
		for(let i=0;i<arr.length;i++){
			console.log(arr[i]);
			if(arr[i]>num){
				return '存在>'+num+'的';
			}
		}
		return '不存在>'+num+'的';
	}
	var res=cunzai(arr);
	console.log(res);
	alert(res)*/

	// 2.判断数组是否都    >0  或  <0   的数
	/*var arr=[-3,-1,0,6,12,65,1,-4];
	function cunzai(arr){
		for(let i=0;i<arr.length;i++){
			console.log(arr[i]);
			if(arr[i]>0){
				return '不是都<0';
			}
		}
	}
	var res=cunzai(arr);
	console.log(res);*/
	
	//	3.筛选 数组元素>0 的元素
	/*	var arr=[-3,-1,0,6,12,65,1,-4];
	function cunzai(arr){
		let arr1=[];
		for(let i=0;i<arr.length;i++){
			console.log(arr[i]);
			if(arr[i]>0){
				arr1.push(arr[i]);
			}
		}
		return arr1;
	}
	var res=cunzai(arr);
	console.log(res);*/
	
	
	//	4.删除重复的元素
	//检查数组中是否包含特定的元素
	/*var arr=[3,-1,1,6,12,-1,65,1,-4];
	function youmeiyou(str,str1){
		for(i=0;i<str.length;i++){
			if(str1==str[i]){
				return true;
			}
		}
//		if(str.includes(str1)){
//			return true;
//		}else{
//			return false;
//		}
		return false;
	}
	//去掉数组中重复的元素
	function delrepeat(arr){
		let newarr=[];
		for(let i=0;i<arr.length;i++){
			let flag=youmeiyou(newarr,arr[i]);
			if(!flag){
				newarr.push(arr[i]);
			}
//			newarr.push()
		}
		return newarr;
	}
	let res=delrepeat(arr);
	console.log(res);*/



	//	5.从数组中随机获取任意元素
	/*var arr=[3,-1,1,6,12,-1,65,1,-4];
	function randomEle(arr,times=3){
		let newarr=[];
		for(let i=0;i<times;i++){
			var num=Math.random()*arr.length;
			var index=arr[Math.floor(num)];
			newarr.push(index);
		}
		return newarr;
	}
	let res1=randomEle(arr);
	console.log(res1);*/
	
	
	

	//	6.从数组中随机获取任意一个不重复的元素
	var arr=[3,-1,1,6,12,-1,65,1,-4];
	function randomEle(arr,times=3){
		let newarr=[];
		for(let i=0;i<times;i++){
			let num=Math.random()*arr.length;		//随机数
			let index=Math.floor(num);				// 向下取整后 的 下标
			while(newarr.includes(arr[index])){			//去重
				num=Math.random()*arr.length;		//随机数
				index=Math.floor(num);				// 向下取整后 的 下标
			}
			newarr.push(arr[index]);
		}
		return newarr;
	}
	let res1=randomEle(arr);
	console.log(res1);











#  数组对象   ????????????????????????????????????????????????????????
//			var arr=[5,1,2,3,4];
//			alert(arr.length);

			
			//从大往小
			arr.sort(function(a,b){
				if(a>b){
					return -1;
				}else if(a==b){
					return 0;
				}else if(a<b){
					return 1;
				}
			});
			document.write(arr);




#事件
	onclick   			鼠标点击事件
	onmouseover   		鼠标经过事件
	onmouseout	 		鼠标移开事件
	onfocus				光标聚焦事件
	onblur				光标失焦事件
	onselect			内容选中事件
	onchange			文本框内容改变事件
	onload				加载事件

	input.focus();//立即获取焦点

###### onclick


#	★★★★★★★★★★★★日期对象★★★★★★★★★★★★★★★★

	//			获取时间:
				var date=new Date;
	//			var date2=new Date("2017/5/1 12:0.0");
	//			var date3=new Date("12:0.0 2017/5/1");
	//			var date4=new Date(2017,4,1,12,0,0);//  月份需要-1.想要输出5月，需要输入4月。

	//可以设置  年、月、日、时、分、秒。不能设置星期几。

			var date=new Date;
			document.write(date.getMonth()+1+'月<br>');   //月份需要+1
			document.write(date.getFullYear()+'年<br>');
			document.write(date.getDate()+'号<br>');
	//		document.write(date.getTime()+'秒<br>');

			var date=new Date;
			date.setFullYear(2018);
			date.setMonth(4);
			date.setDate(1);
			document.write(date+'天<br>');

####	//五一倒计时
		<script>
			var date=new Date;
			function time(){
				var date5=new Date('2017/5/1');
				var date=new Date;
				var cha=Math.floor((date5-date)/1000);  //转换为秒
				var day = Math.floor(cha/(60*60*24));   //转换为天
					cha = cha % (60*60*24);
				var hour=Math.floor(cha/(60*60));		//转换为小时
					cha = cha % (60*60);
				var min =Math.floor( cha / 60);			//转换为分钟
				var second = cha % 60;					//转换为秒
				document.body.innerText=(day+'天'+hour+'小时'+min+'分'+second+'秒');
			}
			time();
			setInterval(time,1000);
		</script>
		
		//十分钟倒计时
		var date1=new Date;
			var date2=date1.setMinutes(date1.getMinutes()+1);
			var date3=date2; 
			function time2(){
				var date4=new Date;
				var cha=Math.floor((date3-date4)/1000);
				while(cha<=0){
					alert('时间到！');
					clearInterval(t);
					return;
				}
				var min=Math.floor(cha/60);
				var second=Math.floor(cha%60);
				document.body.innerText=(min+'分'+second+'秒');
			}
			time2();
			var t=setInterval(time2,1000);
			t;



/*
#################################################################################3
#	★★★★★★★★★★★★ BOM ★★★★★浏览器模型★★★★★★★★★★★★★★★★★★★
#################################################################################3			
*/

#	BOM(Browser Object Model) --浏览器对象模型
	window对象 是BOM中所有对象的核心 --> Global

###	属性
	1.(位置类型)
	(获得浏览器的位置)
	IE:
*	window.screenLeft 可以获得浏览器距屏幕左上角的左边距
*	window.screenTop 可以获得浏览器距屏幕左上角的上边距
	FF: w3c
*	window.screenX 	window.screenY
	(获得浏览器的尺寸)
*	window.innerWidth 获得窗口的宽度
*	window.innerHeight 获得窗口的
*	
	兼容:
*			document.documentElement. clientWidth
*			document.documentElement. clientHeight
	(获得浏览器的分辨率)
*	window.screen.height;
*	window.screen.width;

举例：
/*	console.log(window.screenX);			//距屏幕左边的距离
	console.log(window.screenLeft);
	console.log(window.screenY);			//距屏幕上边的距离
	console.log(window.screenTop);

	console.log(window.innerWidth);			//获取浏览器宽度
	console.log(window.innerHeight);		//获取浏览器高度
	console.log(document.documentElement.clientWidth);		//兼容 宽度
	console.log(document.documentElement.clientHeight);		//兼容 高度

	console.log(window.screen.height);			//屏幕分辨率
	console.log(window.screen.width);*/

###	2.关系类型
	A.top 返回顶层窗口
	B.self === window
	3.status 设置窗口状态栏的文本
	window.top

###	方法:
*	1.窗体控制
		A.对窗体的移动
	window.moveBy(x,y) 相对于当前位置沿着X\Y轴移动指定的像素，	如负数是反方向
	moveTo(x,y) 相对于浏览器的左上角沿着X\Y轴移动到指定的像素，	如负 数是反 方 向
		B.窗体尺寸的改变
	resizeBy(x,y) 相对于当前窗体的大小，调整宽度和高度
	resizeTo(x,y) 把窗体调整为指定宽度和高度
*	2.对窗体滚动条的控制
	scrollBy(x,y) 相对于当前滚动条的位置移动的像素(前提有滚动条)
	scrollTo(x,y) 相对于当前窗口的高度或宽度，移动到指定的像素
			console.log(window.moveBy(20,30));     //移动
			window.scrollBy(200,130);			scrollBy() 可把内容滚动指定的像素数。

###	3.时间间隔的函数
	setInterval(函数指针,指定的时间(毫秒))		按照指定的周期(毫秒)不断的执行函数
	clearInterval() 清除时间函数进程
			setInterval(miaosha,1000)  //  1000毫秒=1秒

	setTimeout(函数指针,指定的时间(毫秒))			在指定的毫秒数后只执行一次函数
	clearTimeout() 清除时间函数进程

###	其他方法:
	alert() 显示带有一段消息和一个确认按钮的警告框。
	confirm() 显示带有一段消息以及确认按钮和取消按钮的对话框。
	prompt() 显示可提示用户输入的对话框。
	close() 关闭浏览器窗口。
	open(url,name,feafurse,replace) 通过脚本打开新的窗口URL要在新窗口中显示的文档的 URL。如果省略了这个参数,那么新窗口就不会显示任何文档
	
	var input=prompt('输入',' ');  //都是字符串
	var flag=confirm(123); 
	open('error.html','_blank','width=500,height=500,left=200,top=100');
	open('error.html','_self','width=500,height=500,left=200,top=100');


/*			
#################################################################################3
					练习
#################################################################################3			
*/

###	//按照指定的周期不停的执行某个函数
	setInterval(function(){
	//	alert(1);
	},1000)  //  1000毫秒=1秒

	setInterval(miaosha,1000)  //  1000毫秒=1秒

	var t = setInterval(miaosha,1000)  //  1000毫秒=1秒
	clearInterval(t);

###	//只执行一次
	var t = setTimeout(miaosha,1000)  //  1000毫秒=1秒
	clearTimeout(t);





/*			
#################################################################################3
					history   location  
#################################################################################3			
*/
	History 对象包含用户(在浏览器窗口中)访问过的 URL ，他是window对象的子对象。
	alert(history.length)

##	属性:
	length 返回浏览器历史列表中的 URL 数量。		alert(history.length)
方法:
	back() 加载 history 列表中的前一个 URL。		history.back();
	forward() 加载 history 列表中的下一个			history.forward();
	go() 值：1 后一个 || -1 前一个 || 0 刷新


#	事件三要素
<script>
//		alert(history.length)
//		操作谁		怎么样		干什么
		alert(3);
		window.onload=function(){
			alert(1);
		}
		alert(2);
		//弹出顺序： 3--2--1  需要页面资源加载完毕之后才能触发window
</script>

###	属性:http://baidu.com/boke/image?
	– hash 设置或返回从井号 (#) 开始的 URL（锚）。
	– host 设置或返回主机名和当前 URL 的端口号。
	hostname 设置或返回当前 URL 的主机名。
	– href 设置或返回完整的 URL。			location.href='error.html';
	– pathname 设置或返回当前 URL 的路径部分。
	– port 设置或返回当前 URL 的端口号。
	– protocol 设置或返回当前 URL 的协议。
	– search 设置或返回从问号 (?) 开始的 URL（查询部分）。
	– http://baidu.com/admin/aaa/#top?name=zhangsan&age=12
	http://127.0.0.1:8020/js-4-27/denglu.html ？

*	协议   	域名  			路径  			 查询	
	hash:   #后边的东西
	
	herf:	整个地址
	pathname:	路径
	pro   协议
	search	?


###	方法:
	– assign() 加载新的文档。   加载文档后会在历史记录里面留下记录
				location.assign('error.html');
	– reload() 重新加载当前文档。
				location.reload('error.html');
	– replace("1,html") 用新的文档替换当前文档。  不会留下记录




################################################################
		举例 -- 页面跳转和 历史刷新
################################################################
<script>
		document.write(history.length);
		window.onload=function(){
			let forward1=document.getElementById('forward');
			let back1=document.getElementById('back');
			let go1=document.getElementById('go');
			forward1.onclick = function(){
				history.forward();
				alert('onclick--forward1');
			}
			back1.onclick = function(){
				alert('onclick--back1');
				history.back();
			}
			go1.onclick = function(){
//				alert(3);
				location.reload();
			}
		}
	</script>
	<body>
		<h1>这是html2页面  </h1>
		<a href="index.html">跳转到 index1 页面</a>
		<button id="forward">2前进</button>
		<button id="back">2后退</button>
		<button id="go">2刷新</button>
	</body>
	
######、、、、、、、、、、、、##########、、、、、、、、、、、##########


###	#############################################################
		举例 -- 登录-出错- html文件
###	#############################################################



################################################################
#	★★★★★★★★★DOM★★★★★★★★★
################################################################

#	document对象
###	一、属性
	title 返回或设置当前文档的标题
	URL 返回当前文档的url
	bgColor 设置文档的背景色
	fgColor 设置文档的前景色(设置文字颜色)

		document.title='曹越';
		console.log(document.title);
		console.log(document.URL);
		document.bgColor='res';
		document.fgColor='red';

###	二、方法:
*	 getElementById(idname)
	返回拥有指定id的（第一个）对象的引用
*	 getElementsByTagName(tagname)
	获得的是集合（类似于数组），需要加下标[0].元素都需要加下标
	返回带有指定标签名的对象的集合
*	 getElementsByName(name)
	返回带有指定name指定名称的对象的集合
*	 getElementsByClassName()
	返回带有指定class指定名称的对象的集合

###	Document 对象集合
	A. all 所有元素的集合
	B. forms 返回对文档中所有form对象的引用
		通过集合来访问相应的对象
			1.通过下标的形式
			2.通过name形式
	C. anchors 返回对文档中所有anchors(锚链接) 对象的引用
	D. images 返回对文档中所有image 对象的引用
	E. links 返回对文档中所有area 对象和link对象的引用
	







################################################################
						事件
################################################################

##	一、事件驱动
	1.事件
	javascript侦测到的用户的操作或是页面 的一些行为(怎么
	发生的)
	2.事件源
	引发事件的元素。(发生在谁的身上)
	3.事件处理程序
	对事件处理的程序或是函数 (发生了什么事)


##	1.常用的鼠标事件
	 onclick 鼠标单击事件
	 ondblclick 鼠标双击事件
	 onmousedown 鼠标按下事件
	 onmouseup 鼠标抬起事件
	 onmousemove 鼠标移动事件     鼠标在规定区域、块儿内移动时的效果
	 onmouseover 鼠标移入事件 移入其子元素，仍会触发
	 onmouseout 鼠标移出事件
	   onmouseenter 鼠标移入事件  移入，常用
	 onmouseleave 鼠标移出事件   移出，常用

##	2.键盘事件
	 onkeyup 按键弹起事件
	 onkeydown 按键按下事件
	 onkeypress 按键按下或按住


##	3.表单事件
	onsubmit
	onblur
	onfoucs
	onchange


##	4.页面事件
	 onload 页面加载


################################################################
			对内容、属性、样式的操作
################################################################

	操作属性
	对象.属性
	对象.属性=值 (设置、获取、添加属性 (属性值))

	对样式的操作:
	1.批量修改
	– 通过ID来更改样式
	– 通过className更改样式
	2.通过行内样式更改
	– 对象.style.属性(获取)
	– 对象.style.属性=值 (设置、更改、添加属性)




#	★★★★对内容、属性、样式的操作★★★★★★★★★

###	行内样式和外部样式通用的获取方法  获取样式属性
* 对象.currentStyle.属性 IE 用来获得实际的样式属性
* getComputedStyle(对象,null).属性 FF 用来获得实际的样式属性
* 只能获取不能设置
#####
	window.onload=function(){
		let box1=document.getElementsByClassName('box');
		console.log(getComputedStyle(box[0],null).width);
		console.log(getComputedStyle(box[0],null).height);
			//可以获取所有，但只能获取，不能设置
	}

#####  让块儿反复伸缩
	window.onload=function(){
		let box1=document.getElementsByClassName('box')[0];

		var t= setInterval(resize, 200);
		let speed=10;
		function resize(){
			let widths= parseInt(getComputedStyle(box1,null).width);
			if(widths>=400){
				widths=400;
				speed*=-1;
			}
			if(widths<=300){
				widths=300;
				speed*=-1;
			}
			box1.style.width=`${widths+speed}px`;
		}


		/*let flag=1;
		function resize(){
			let widths= parseInt(getComputedStyle(box1,null).width);
			box1.style.width = widths+10+'px';
			if(flag==1){
				box1.style.width = widths+10+'px';
				console.log(box1.style.width);
				if(box1.style.width >'400px'){
					flag=2;
				}
			}
			if(flag==2){
				box1.style.width = widths-10+'px';
				console.log(box1.style.width);
				if(box1.style.width <'300px'){
					flag=1;
				}
			}
		}*/


### 操作内容
1.innerHTML 用来设置或获取对象起始和结束标签内的内容(识别html标签)
2.innerText 用来设置或获取对象起始和结束标签内的文字内容 (IE)
textContent用来设置或获取对象起始和结束标签内的文字内容 (FF)

<script>
	window.onload=function(){
		let box=document.getElementsByClassName('box')[0];
		console.log(box.innerText);
		box.innerText='设置text文本';
		console.log(box.innerHTML);
		box.innerHTML='设置innerHTML属性';
		console.log(box.outterText);
		console.log(box.outterHTML);

		box.className='box hot';
		box.id
		btn.zhangsan
	}
</script>


querySelectorAll
返回指定选择器的集合，需要加下标。
querySelec
返回指定选择器的第一个，直接操作，不需要加下标。


input1[i].onmouseover=function(){
	// this.style.background='red';	等同于下一句
	input1[i].style.background='red';
	kw[i].style.height='200px';
	let a=this;
	function aa(){
		input1[i].style.background='red';
		// this.style.background='red';
		这儿的this需要上边 let =this 一下，否则不能用。
	}
}



#	★★★★封装 ★★★★★★★★★★★★
###  js 文件
	//    去空   判断类型   判断字符串	判断 . #    获得 字符串
	function $(selector,ranger=document){
		let type=typeof selector;
		if(type == 'string'){
			//元素的获取
			let select = selector.trim();
			let first = select.charAt(0);
			if(first=='.'){
				return ranger.getElementsByClassName(select.substring(1));
			}else if(first=='#'){
				return document.getElementById(select.substring(1));
			}else if(/^[a-zA-Z][a-zA-Z1-6]{0,8}$/.test(select)){     // 正则//    ^开头   $结尾
				return ranger.getElementsByTagName(select);
			}
		}else if(type=='function'){
			//添加事件
			window.onload=function(){
				selector();
			}
		}
	}



###	★★★★★★★★★如何实现兼容★★★★★★★★★★★★★★
	function getStyle(boj,attr){
		if(window.getComputedStyle){
			// alert(1);
			return getComputedStyle(obj,null)[attr];
		}else{
			alert(2);
			return obj.currentStyle[attr];
		}
	}

###	★★★★★★设置或获取某一个元素的内容★★★★★★★★
`/*html(obj,contant)	 
obj  指定的对象		
contant	设置的内容 ，没有--》表示获取内容	有--》  设置内容*/`
###
	function html(obj,content){  	
	//content  没传 就是undefined  就是false
		if(content){
			// 》设置
			return obj.innerHTML=content;
		}else{
			// 获取
			return obj.innerHTML;
		}
	}

	/*
	html(obj,contant=neitong)
###	设置或获取某一个元素的内容	
	obj  指定的对象
	contant	设置的内容 ，
	没有--》表示获取内容
	有--》  设置内容
	*/

	function html(obj,content){  	
	//content  没传 就是undefined  就是false
		if(contant){
			// 》设置
			obj.innerHTML=content;
		}else{
			// 获取
			return obj.innerHTML;
		}
	}


##	//动画封装   多参数输入
		/*animate(box,{width:500,height:400,left:500}，function(){ }) 
		function animate(obj,attrObj){
			let speed=10;
			t=setInterval(move,200);
			function move(){
				for(let i in attrObj){
					let currentV=parseInt(getComputedStyle(obj,null)[i])+10;
					if(currentV>=attrObj[i]){
						currentV=attrObj[i];
						clearInterval(t);
					}
					obj.style[i] = currentV+'px';
				}
			}
		}*/

#### 自动轮播
	//		状态初始化
	//		  current（当前窗口）   next（下一个）
	//		 就位  next   left:width	
	//		 动画		
	//			index	left:-width;	
	//			next	left:0
	//		更新	  current

		
		let imgbox=document.querySelector('.imgbox');
		let imgs=document.querySelectorAll('.imgbox li');
		let imgwidth=parseInt(getComputedStyle(imgbox,null).width);
		let current=0,next=0;
		let t;
		for(let i=0;i<imgs.length;i++){
			if(i==0){
				continue;
			}
			imgs[i].style.left=imgwidth+'px';
		}
		t=setInterval(move,2000);
		function move(){
			next++;
			if(next==imgs.length){
				next=0;
			}
			imgs[next].style.left=imgwidth+'px';
			animate(imgs[current],{left:-imgwidth});
			animate(imgs[next],{left:0});
			current=next;
		}

####手动轮播
	//  手动点击轮播点 向左切换图      OK
		for(var i=0;i<btns.length;i++){
			btns[i].index=i;   //用index保存对应属性 和 值
			btns[i].onclick=function(){
	//				alert(this);
	//				alert(this.index);
				btns[current].className=''; //轮播点
				this.className='hot';
				imgs[this.index].style.left=imgwidth+'px';
				animate(imgs[current],{left:-imgwidth});
				animate(imgs[this.index],{left:0});
				current=next=this.index;
			}
		}

#####	？？？？？？？？？？？？？？？？？？？？？？？？？？？ 
	手动点击轮播点   向左   向右   切换图

		//   value  对应元素     index 对应下标   obj对应对象
		btns.forEach(function(value,index,obj){
			//index 对应 next
			value.onclick=function(){
				if(current==index){
					return;
				}
				btns[current].className=''; //轮播点
				btns[index].className='hot';
				if(index>current){
					btns[index].style.left=imgwidth+'px';
					animate(imgs[current],{left:-imgwidth});
					animate(imgs[index],{left:0});
				}else if(index<current){
					btns[index].style.left=-imgwidth+'px';
					animate(imgs[current],{left:imgwidth});
					animate(imgs[index],{left:0});
				}
				current=next=index;
			}
		})

###		闭包函数
	let bb==aa(321);
	bb();
	function aa(j){
		return function(){
			alert(j);
		}
	}

外层函数调用内层函数的局部变量


内存泄漏：

#####   使用forEach	？？？？？？？？？？？？？？？？？？？？？？？
		let btns1=document.getElementsByClassName('btn')[0];
		let aa=btns1.getElementsByClassName('li')[0];
		console.log(Array.from(aa));
//		转化成数组 就可以用  forEach 了
		//冒充法
		Array[0].forEach.callback

###   获取 box 宽高 尺寸  获取位置
	let widths1=box.offsetWidth;
	let height=box.offsetHeight;
	let top=box.offsetTop;
	let left=box.offsetLeft;
*	只有 top left  没有right和bottom

	let cw=window.innerWidth;浏览器宽度
	let ch=window.innerHeight;浏览器高度

*	scrollTop
*	scrollLeft
*	获取具有滚动条元素的位置属性.具有滚动条的元素在滚动的时候，他的内部元素超出该元素顶部或是左边的距离。
	`let a=document.body.scrollTop`

#	按需加载
	window.onscroll=function(){   //  按需加载  方法二   OK
		let tops=document.body.scrollTop;
		for(let i=0;i<arr.length;i++){
			if(tops+ch>arr[i]+100){
				let floor=document.getElementsByClassName('floor')[i];
				let imgs=floor.getElementsByTagName('img');
				for(let j=0;j<imgs.length;j++){
					imgs[j].src=imgs[j].title;
					console.dir(imgs[j].src);
				}
			}
		}
	}
	
	/*window.onscroll=function(){     //  按需加载  方法一  OK
		let tops=document.body.scrollTop;
		arr.forEach(function(value,index){
			if(tops + ch > value+50){
				//index  下标
				let floor=document.getElementsByClassName('floor')[index];
				let imgs=floor.getElementsByTagName('img');
				for(let i=0;i<imgs.length;i++){
					imgs[i].src=imgs[i].title;
					console.dir(imgs[i].src);
				}
			}
		})
	}*/


##  类名操作
*	
*	sli[i].classList.add('hot');   //添加类名
*	sli[i].classList.remove('two');  //删除类名
*	sli[i].classList.toggle('two');  //以前有，则删除
*	sli[i].classList.toggle('three');  //以前无，则添加

*	sli[n].className='';
*	this.className='hot';

#####for( let i in
	let a=document.body.scrollTop
	//		console.log(a);

###	过渡结束
*	ontransilationEnd


#	节点的属性和方法
#####获得节点关系的属性
*	对象.parentNode 获得父节点的引用
*	对象.childNodes 获得子节点的集合
*	对象.firstChild 获得第一个子节点的引用
*	对象.lastChild 获得最后一个子节点的引用
*	对象.nextSibling 获得下一个兄弟节点的引用
*	对象.previousSibling 获得上一个兄弟节点的引用

	var one = div1.nextElementSibling || div1.nextSibling;
	// 所以用这种处理兼容的办法：中间通过一个变量，获取其中一个值   
	注意：先写正常浏览器，在写要去兼容的IE其他浏览器

####  eg:
	let box=document.getElementsByClassName('box')[0];
	let child=box.childNodes;
	let son = child[1];
	son.style.background='yellow';
	let prev=son.previousSibling;
	let par=son.parentNode;
	console.dir(son);
	console.dir(prev);
	console.dir(par);


##  封装 获取 第一  最后一个  元素节点


#### 创建指定元素    创建一个div:
	let button=document.querySelector('button');
	button.onclick=function(){
		let ele=document.createElement('div');
		ele.style.cssText='width:200px;height:200px;background:red';
		document.body.appendChild(ele);
	}

####   创建 id  class
	ele.id='one';
	ele.className='two';


##	节点的方法
	一、创建节点
	1. 创建元素节点
	document.createElement("元素标签名");
	2. 创建属性节点
	A.对象.属性="属性值“
	B.对象.setAttribute(属性名,属性值)
	C. arrt=document.createAttribute(“属性名”);
	arrt.nodeValue=“属性值”
	obj.setAttributeNode(arrt);
	3. 创建文本节点
	对象.innerHTML="";
	document.createTextNode("文本");

##	插入元素
*	document.body.appendChild(ele);   //父元素的后面插入
*	document.body.insertBefore(ele,box);  //往指定元素的前面插入，在 box之前插入 ele

	obj.insertBefore(ele,box);   // obj(父元素).在box之前插入ele

	obj 父元素
	ele 要插入的元素
	box  在其之前插入新节点的子节点。如果未规定，则 insertBefore 方法会在结尾插入 newnode。


##	三、删除节点
*	父对象.removeChild(删除的对象)
	如果确定要删除节点，最好也清空内存 对象=null;

	let box=document.querySelector('.box');
	document.body.removeChild(box); //移除box
	box=null; //移除对象，从内存中清空对象


###  四.替换
*	document.body.replaceChild(ele.box);

	let newbox=box.cloneNode();   //只克隆节点本身，不可隆内部元素
	let newbox=box.cloneNode(true);   //克隆节点本身+内部元素
	document.body.appendChild(newbox);

###	maspainter


####	//设置背景颜色    方法一   OK
	let colorArr=[0,3,6,9,'c'];
	function getColor(){
		let color='#';
		for(let i=0;i<3;i++){
			let num=Math.floor(Math.random()*colorArr.length);
			color+=colorArr[num];
		}
		return color;
	}

####	//设置背景颜色    方法二  
	function getColor(){
		let r= Math.floor(Math.random()*256);
		let g= Math.floor(Math.random()*256);
		let b= Math.floor(Math.random()*256);
		return `rgb(${r},${g},${b})`;
	}

###		轮播  向左 左移     index轮换图.html
	function move(){    //左移
		animate(imgbox,{left:-widths},function(){
			let first=getFirst(imgbox);
			imgbox.appendChild(first);
			imgbox.style.left='0';
		})
	}


#	事件绑定  事件详情
	1.一般绑定事件
	在脚本中绑定  报错
	直接在HTML元素绑定
	*	2.同一个事件绑定多个事件处理程序
	IE:
	对象.attachEvent("事件(on)",move) 添加
	对象. detachEvent("事件(on)","处理程序") 删除
	FF:
	对象.addEventListener("事件","处理程序",布尔值) 添加
	对象.removeEventListener("事件","处理程序",布尔值) 删除


###		绑定事件方式：	
	// 绑定事件方式：一		事件类型  事件处理函数  布尔值
	// box.addEventListener('click',function(){alert(1),false});

	// 绑定事件方式： 二
	function aa(){alert(1)};
	function bb(){alert(2)};
	box.addEventListener('click',aa,false);
	box.addEventListener('click',bb,false);

	box.onclick=function(){
		aa();
		bb();
	}
	box.onclick=null;

##	一、事件驱动
	1.事件
	JavaScript侦测到的用户的操作或是页面的一些
	行为(怎么发生的)
	2.事件源
	引发事件的元素。(发生在谁的身上)
	2.事件处理程序
	对事件处理的程序或是函数 (发生了什么事)

###	一、什么是事件对象
	用来记录一些事件发生时的相关的信息的对象
	1.只有当事件发生的时候才产生，只能在处理函数内部访问
	2.处理函数运行结束后自动销毁。
	二、如何获取事件对象
	IE：window.event
	FF: 对象.on事件=function (e){}

#	1.关于鼠标事件
	相对于浏览器位置的
	clientX 当鼠标事件发生的时候，鼠标相对于浏览器X轴的位置
	clientY 当鼠标事件发生的时候，鼠标相对于浏览器Y轴的位置
	相对于屏幕位置的
	screenX 当鼠标事件发生的时候，鼠标相对于屏幕X轴的位置
	screenY 当鼠标事件发生的时候，鼠标相对于屏幕Y轴的位置
	相对于事件源的位置
	offsetX 当鼠标事件发生的时候，鼠标相对于事件源X轴的位置
	offsetY 当鼠标事件发生的时候，鼠标相对于事件源Y轴的位置

###	关于鼠标滚轮的   onmousewheel
	滚轮事件
	if(document.attachEvent){
	document.attachEvent("onmousewheel",scrollFn); //IE、 opera
	}else if(document.addEventListener){
	document.addEventListener("mousewheel",scrollFn,false);
	//chrome,safari -webkitdocument.addEventListener("DOMMouseScroll",scrollFn,false);
	//firefox -moz-
	}


	事件对象属性:
###  滚轮   onmousewheel
	事件对象.wheelDelta 获取滚轮滚动的方向 IE
	事件对象.detail 获取滚轮滚动的方向 FF

 	let box=$('.box')[0];
	console.log(box.style.height);
	document.addEventListener('mousewheel',function(e){
	   let dir=e.wheelDelta;
	   if(dir==120){    //  谷歌  滚轮朝下 -120  滚轮朝上 120    火狐  下  3  上  -3
	       //up
	        box.style.height=510+'px';
	   }else if(dir == -120){
	       //下
	       box.style.height=50+'px';
	   }
	},false)

###	let box=$('.box')[0];    鼠标滚动  变色
	mouseWheel(box,function(){
	   box.style.background='green';
	},function(){
	   box.style.background='blue';
	})

	
####	关于鼠标移入移出的
	mouseout mouseover
	事件对象属性
	事件对象.fromElement 鼠标从哪来 IE
	事件对象.toElement 鼠标到哪去 IE
	事件对象.relatedTarget FF
	在mouseover事件中代表IE中的fromElement
	在mouseout事件中代表IE中的toElement

### 2.关于键盘事件   不区分大小写  a-A都是65
	keyCode 获得键盘码
	空格:32 回车13 左上右下：37 38 39 40
*	altKey 判断alt键是否被按下 按下是true 反之是false 布尔值
*	ctr
*	lKey
*	shiftKey
*	type 用来检测事件的类型 主要是用于多个事件通用一个事件处理程序的时候
	e.type=='click'   ***e.type=='keydown'***

*	 onkeyup 按键弹起事件
*	 onkeydown 按键按下事件
*	 onkeypress 按键按下或按住

##   事件流
	当页面元素触发事件的时候，该元素的容器以及整个页面都会按照特定顺序响应该元素的触发事件，事件传播的顺序叫做事件流程。
	事件流的分类
	1.冒泡型事件(所有的浏览器都支持)   从下往上   
	
	由明确的事件源到最不确定的事件源依次向上触发。
*	***addEventListener(事件，处理函数，false)***
   IE低版本中只有冒泡型从下往上
 	onEventType addEventListener
  ***同类型事件*** 才会响应 冒泡
	
	2.捕获型事件(IE不支持 w3c标准 火狐)  从上往下
	不确定的事件源到明确的事件源一次向下触发。
	addEventListener(事件，处理函数，true)

  目标事件源对象  e.target
	是谁触发的该事件

###  事件源 事件对象  目标事件源的对象

box e.target (box,)

	
###	阻止事件流(事件对象)
*	e.preventDefault();  清除浏览器默认行为
*	e.stopPropagation(); 阻止事件流

	IE: 事件对象.cancelBubble=true;
	FF: 事件对象.stopPropagation();
*	获得目标事件源的对象
	IE： 事件对象.srcElement
	FF: ***事件对象.target***

*	事件对象阻止浏览器默认行为
	if (ev.preventDefault )
	ev.preventDefault(); //阻止默认浏览器动作(W3C)
	else
	ev.returnValue = false;//IE中阻止函数器默认动作的方
	式

##	 事件委派   son -> box
	把原来加给子元素身上的事件绑定在父元素身上，就是把事件委派给父元素
	box.onclick=function(){
		box.target.style.background='red';
		//实际操作为box的son 
	}
*	有大量的事件需要处理的时候
*	通过JS动态，后添加的元素，需用委派  e.target

###  举例： 键盘点击+鼠标点击 = 评论页面
	btn.onclick=text.onkeydown=function(e){
		if(text.value.trim()==''){
			return;
		}
		if(e.type=='click'){
			let news=document.createElement('li');
			let new1=document.createElement('div');
			new1.className='delete';
			news.innerText=text.value;
			// new1.innerText='X';
			new1.innerText='删除';
			ul.appendChild(news);
			ul.appendChild(new1);
			text.value='';
			span.innerText='100';
			console.log('OK');
			new1.onclick=function(){
				ul.removeChild(new1);
				ul.removeChild(news);
			}
		}else if(e.type=='keydown'){
			if(e.shiftKey&&e.keyCode==13){
				let news=document.createElement('li');
				let new1=document.createElement('div');
				new1.className='delete';
				news.innerText=text.value;
				new1.innerText='X';
				ul.appendChild(news);
				ul.appendChild(new1);
				text.value='';
				span.innerText='100';
				console.log('OK');
				new1.onclick=function(){
					ul.removeChild(new1);
					ul.removeChild(news);
				}
			}
		}



#  Cookie 是一些数据, 存储于你电脑上的文本文件中。
当 web 服务器向浏览器发送 web 页面时，在连接关闭后，服务端不会记录用户的信息。
Cookie 的作用就是用于解决 "如何记录客户端的用户信息":

##  cookie
*	name cookie名
*	value 值
*	expires 过期时间
*	path 路径

#####	设置 生成 cookie：
	document.cookie=`${key}=${value};expires=${expires.toUTCString()}`;
	document.cookie='name=liujiang';
    document.cookie='age=18';
    document.cookie='sex=nan;expires='+time.toUTCString();

*	function setcookie
*	function getcookie
*	function delcookie



##	localStorage  本地存储   页面之间可以共享
	不删除 就会 永久性存在
*	    localStorage.setItem('class','1702');
*	    设置（名字，值）
*	    localStorage.getItem('class');
*	    获取（名字）
*	    localStorage.key(0);
*	    localStorage.clear();
*	    清除
*	    localStorage.removeItem('name');
*	    移除

##	sessionStorage
	用法和 localStorage 一样  。页面之间不能共享
	临时的，关了浏览器就没了
*    sessionStorage.aa='bb';    //设置aa的值是bb


###   cookie--localstorage--sessionstorage 区别
*	1.localStorage、sessionStorage（5M）  比cookie（4K） 容量大，存储方便
*	2.cookie存储有时间限制，设置就有，不设置就是临时的，关闭浏览器就没了。localStorage 必须手动清除，不删除 就会 永久性存在。 sessionStorage临时的。关闭浏览器就没了。
*	3.删除方式： cookie 需要把时间设置提前。localStorage、sessionStorage是remove和clear.
*	4.localstorage 页面之间可以共享.  sessionstorage 页面之间不能共享


	`localStorage    5M     必须手动清除   remove   clear

	`sessionStorage   5M   关浏览器就没了    remove   clear

	`cookie 区别      有时间  设置就有，不设置就是临时的，关浏览器就没了。内
	存少 4k    删除方式   需设置，把时间提前`



##    JSON.parse      /字符串转化成对象
##     JSON.stringify   对象转换为一个JSON字符串
    let student1 =localStorage.student;
    let json1=JSON.parse(student1);   //字符串转化成对象
    console.log(json1[0]);
    json1.push({'name':'zhangsan','age':18});
    localStorage.student = JSON.stringify(json1);   //对象转化成字符串
                                                        //将一个JavaScript值转换为一个JSON字符串


音频、视频
video
type  设置格式


#  音频、视频    video   audio

audio.muted   静音


# canvas
画板  画布

## 标签
`<canvas widht="300px" height="300px">替换内容</canvas>`
不能在CSS中设置宽高

##尺寸
*	width
*	height
>   CSS相当于放大

##  坐标
>   原点左上角；水平 X Y

##  绘图环境  2D
let ctx = canvas.getContext('2d'); //绘 2D 图

##  矩形    （矩形左上角的 x坐标 Y 宽 高)
*	context.rect(x,y,width,height);
*   矩形左上角的 x 坐标  Y坐标  宽 高
*	context.fillRect(x,y,width,height);<br>
*	ctx.fillRect(10,10,100,100);    //填充
*   ctx.strokeRect(200,100,50,50);  //描边
*   ctx.clearRect(50,50,50,50);     //擦除

##  样式
*	fillstyle  设置或返回用于填充绘画的颜色、渐变或模式
*	strokestyle
>   red   #000  rgb()  rgba()  渐变

##	路径
    ctx.beginPath();        //开始   每次都要开始
    ctx.moveTo(150,150);    //移动位置
    ctx.lineTo(150,200);    //绘制
    ctx.lineTo(200,175);    //
    ctx.closePath();        //闭合
	ctx.fillStyle='purple'; //填充为紫色
    ctx.fill();             //填充
    ctx.stroke();           //描边


##	画圆
    ctx.beginPath();
    ctx.arc(150,150,100,0,2*Math.PI);//  250,150
//   （圆心 x 坐标,Y坐标，半径，起始角-以弧度计，结束角-以弧度计，true逆时针/false顺时针）
    ctx.closePath();
    ctx.stroke();

	/* let anglue = (n * 360 / 100) * Math.PI / 180; // 从0开始
       ctx.arc(150,150,50,0,anglue,false);*/
       let anglue = (n * 360 / 100-90) * Math.PI / 180; // 从0开始
       ctx.arc(150,150,50,-Math.PI/2,anglue,false);
//    （圆心 x 坐标,Y坐标，半径，起始角-以弧度计，结束角-以弧度计，true逆时针/false顺时针）

##   贝塞尔   quadraticCurveTo
//    贝塞尔控制点的 x 坐标,	贝塞尔控制点的 y 坐标,	结束点的 x 坐标, 结束点的 y 坐标
    ctx.quadraticCurveTo(50,20,50,50);

##   线
*	linewidth		线宽
*	linecap			端点
*	linejoin		拐点

    ctx.lineWidth = 10;
    ctx.lineCap='round';  // round 圆形线帽
    ctx.lineCap='square'; //方形
    ctx.lineCap='butt';   //默认没有

    ctx.lineJoin='round';//圆角
    ctx.lineJoin='bevel';//平角

    ctx.lineJoin='miter';//尖角
    ctx.miterLimit=4;


##  文本操作 字体
    ctx.font = 'bold 30px 宋体';
    ctx.textAlign = 'right'; //右对齐  对齐方式
    context.textAlign="center|end|left|right|start";
                         居中  结束  左对齐  右对齐  开始
    ctx.textBaseline = 'top'; //文本基线。
    context.textBaseline="alphabetic|top|hanging|middle|ideographic|bottom";
                                    默认   em方框的顶端  悬挂基线 正中  表意基线   方框的底端
    ctx.strokeText('hello world',150,150);  //不填充文本
    context.strokeText(text,x,y,maxWidth);
         画布上输出的文本。 开始绘制文本的 x 坐标， y坐标， 可选。允许的最大文本宽度
    ctx.fillText('hello world',150,200);   //绘制填充色文本

    let aa = ctx.measureText('hello world');   //测量

##  阴影   虚线   setLineDash
	ctx.setLineDash([4, 2]);   //设置虚线，参数为数组，第一个值为实现宽度，第二个值为空白的宽度
    ctx.lineDashOffset = 0;   //虚线起始偏移量
    ctx.shadowColor = 'red'; //阴影颜色
    ctx.shadowBlur = 5;   //阴影的模糊级数
    ctx.shadowOffsetX = 5;         //
    ctx.shadowOffsetY = 5;         //

##  ctx.clearRect(0,0,600,500);  //清空画布



##  ctx.translate(x,y);  //平移原点
##  ctx.rotate(Math.PI/2);   //旋转坐标系 x 度，正方向


## 插入图片
*   context.drawImage(img,sx,sy,swidth,sheight,x,y,width,height);
>	img	规定要使用的图像、画布或视频。
	sx	可选。开始剪切的 x 坐标位置。
	sy	可选。开始剪切的 y 坐标位置。
	swidth	可选。被剪切图像的宽度。
	sheight	可选。被剪切图像的高度。
	x	在画布上放置图像的 x 坐标位置。
	y	在画布上放置图像的 y 坐标位置。
	width	可选。要使用的图像的宽度。（伸展或缩小图像）
	height	可选。要使用的图像的高度。（伸展或缩小图像）

    let img = new Image();
    img.src = '../img_1.png';
    img.onload = function(){  //加载
        ctx.drawImage(img,100,200,200,200)
	}



##		save   restore
>    save() 方法保存当前图像状态的一份拷贝。
>    restore() 方法将绘图状态置为保存值。
    ctx.fillStyle = 'green';
    ctx.fillRect(75,75,200,200);
    ctx.save();							、、、、、、、保存save之前的样式

    ctx.fillStyle = 'yellow';
    ctx.fillRect(100,100,100,100);

//    ctx.fillStyle = 'blue';
    ctx.restore();					、、、、、、、、、、恢复到save之前样式
    ctx.fillRect(125,125,50,50);

#### eg:画板  虚线
    self.ctx.save();
    if(self.arr.length > 0){
        self.ctx.putImageData(self.arr[self.arr.length-1],0,0)
    }
    self.ctx.beginPath();
    self.ctx.moveTo(ox,oy);
    self.ctx.lineTo(mx,my);   //划线
    self.ctx.setLineDash([4, 6]);
    self.ctx.closePath();
    self.ctx.stroke();
    self.ctx.restore();

##  putImageData   getImageData
	putImageData(self.arr[self.arr.length-1],0,0)
	this.ctx.getImageData(0,0,this.width,this.height)


## 	下载
let data = this.obj.toDataURL('image/png').replace(`data:image/png`,'data:stream/octet')

## 	下载图片    
	let imgdata = canvas.toDataURL('image/png'); //创建 
        let img = new Image;
        img.src = imgdata;
        img.onload=function(){
//            for(let i=0;i<box.childNodes.length;i++){
            if(box.childNodes.length ==2 ){
                box.removeChild(box.firstChild);
                box.removeChild(box.lastChild);
            }
            box.appendChild(img);
            let a= document.createElement('a');
            a.href = imgdata;
            a.download = 'qipan.png';   //下载
            box.appendChild(a);
        };


## 正则


###  创建正则表达式
在javascript正则表达式也是通过对象的方式来创建的，他有自己的方法。
*	1. 通过构造函数创建 reg=new RegExp(“正则表达式”,”模式修正符”)
	var reg = new RegExp("uek“);
	var stat = reg.test("sxuek");
	alert(stat);
*	2. 通过字面量方式创建
	var reg = /uek/i;
	var stat = reg.test("sxuek");
	alert(stat);
	通常将正则表达式字符串放在 /RegExp/ 中间//称为定界符



*	RegExp.test(str)	`返回一个 Boolean 值，它指出在被查找的字符串中是否存在模式`

*	RegExp.exec() 	`在字符串中匹配，成功返回数组，失败返回null`
*	console.log(reg1.exec(str1)); //数组：
		//  0:"abc"  index(位置):0   input:"abcdef"    length:1


let str = `a0b12cd345ef67g890h`;
let reg = /abcd123/;  //原子
let reg2 = /[a-z]/g;  //  让他一直往下匹配
let reg1 = /[0-9]/;  //[]原子表  一个[] 代表一位，这一位可以是[]中的任意一个
let reg1 = /[\d]/; 	  //  [0-9]
let reg1 = /[\D]/;   //  [^0-9]    相当于/[\d]/ 取反 == 与除了数字以外的任何一个字符匹配 [^0-9]
let reg1 = /[\w]/;   //  [0-9a-zA-Z]   中任意一个元素
let reg1 = /[\W]/;   //  [^0-9a-zA-Z]  与[\w]取反
			/[\s]/    //  与任意一个空白字符匹配
			/[\S]/	  //  与除了空白符外任意一个字符匹配
\f	换页
\n	换行
\r	回车
\t	制表符
\v	垂直制表
\S	与除了空白符外任意一个字符匹配	[^\n\f\r\t\v]

####  原子表
 [ ] 只匹配其中的一个原子
 [^] 只匹配"除了"其中字符的任意一个原子   取反
 [0-9]　匹配0-9任何一个数字
 [a-z]　匹配小写a-z任何一个字母
 [A-Z]　匹配大写A-Z任何一个字母


####   元字符
在正则表达式中有一些特殊字符带表特殊意义叫元字符。
– . 除换行符以外的任何一个字符
– | 或的意思，匹配其中一项就代表匹配
> 例子:匹配身份证号，旧版是15位数字，新版是18位数字
  `/^\d{15} ¦\d{18}$/`


####   原子分组   反向引用
匹配多个字符时用()分组，分组代表一个原子集合或者说一个大原子，并压入堆栈(内存)用于调用，组号是从左到右.
计数的调用时：如果是字面量形式用\1，构造函数方式用\\1.
这种方式我们叫做反向引用


####   取消反向引用
使用形如(?:pattern)的正则就可以避免保存括号内的匹配结果，反向引用也将会失效


####   模式修正符
 i 不区分大小写字母的匹配
 m 将字符串视为多行，修饰^与$
 g 全局匹配，找到所有匹配项


####	量词
可以使用一些元字符，重复表示一些元子或元字符

	 * 重复零次或更多次
	 + 重复一次或更多次
	 ? 重复零次或一次
	 {n} 重复n次
	 {n,} 重复n次或更多次
	 {n,m} 重复n到m次
	一片两片三四片，落尽正则全找见
	上面的小标题翻译成正则就是{1},{2},{3,4},{1,}

####		禁止贪婪
正则匹配是贪婪的，禁止贪婪用 ?
*	*? 重复任意次，但尽可能少重复
*	+? 重复1次或更多次，但尽可能少重复
*	?? 重复0次或1次，但尽可能少重复
*	{n,m}? 重复n到m次，但尽可能少重复
*	{n,}? 重复n次以上，但尽可能少重复


	let str = `a0b12cd345ef67g890h`;
	let reg = /abcd123/;  //原子
    let reg2 = /[a-z]/g;  //  让他一直往下匹配
	let reg1 = /[0-9]/;  //[]原子表  一个[] 代表一位，这一位可以是[]中的任意一个
	let reg1 = /[\d]/; 	  //  [0-9]
	let reg1 = /[\D]/;   //  [^0-9]    相当于/[\d]/ 取反 == 与除了数字以外的任何一个字符匹配 [^0-9]
	let reg1 = /[\w]/;   //  [0-9a-zA-Z]   中任意一个元素
	let reg1 = /[\W]/;   //  [^0-9a-zA-Z]  与[\w]取反
				/[\s]/    //  与任意一个空白字符匹配
				/[\S]/	  //  与除了空白符外任意一个字符匹配
\f	换页
\n	换行
\r	回车
\t	制表符
\v	垂直制表
\S	与除了空白符外任意一个字符匹配	[^\n\f\r\t\v]


		let reg2 = /[a-z]/;  //   [\d]   [0-9]   [1,2,3,4,5,6,7,8,9,0]  一样
		let result = reg.exec(str);
		console.log(result)

        贪婪匹配：尽可能多的重复

        let str = `a0b12cd345ef67g890h`;
		var reg = /\d{2}/g;
					数字出现2次

        var reg = /\d\w{2,4}/g;
					w至少2次，最多4次
		           满足情况下尽可能的多

        var reg = /\d\w{2,}/g;
        			   \w至少2次，然后尽可能的多

        var reg = /\d\w*/g;
        var reg = /\d\w{0,}/g;
        				\w* 重复零次或更多次

        var reg = /\d\w+/g;
        var reg = /\d\w{1,}/g;
        			   \w重复一次或更多次

        var reg = /\d\w?/g;
        var reg = /\d\w{0,1}/g;
        				\w重复零次或一次


var reg = /[a-z][a-z1-6]{0,5}/;
var reg = /^[a-z][a-z1-6]{0,5}$/;
		边界限定符  ^必须以[a-z]开头     $必须以[a-z1-6]结尾
var reg = /^<[a-z][a-z1-6]{0,5}>$/;
创建   边界限定符  ^必须以[a-z]开头     $必须以[a-z1-6]结尾
var str = 'div';

alert(reg.test(str));

var reg = /\bjava\b/;
		\b 单词边界符
var str = 	'javascript html css ';
result = reg.test(str);



###  字符边界

^ 匹配字符串的开始
$ 匹配字符串的结束，忽略换行符
*	单词边界限制
\b 匹配单词的边界
\B 匹配除单词边界以外的部分



##		字符串中用到正则的函数
#### str.search(regexp)
– regexp为正则表达式，反回索引位置，不支持全局索引(即g修饰符无效）找到即停止搜索

####		replace（正则或字符串,替换内容）
支持全局g修饰符，如果模式不是全局，当匹配到一个以后将不会继续匹配，反之则会继续往下匹配。

####		split 方法
– 拆分字符串，参数可以为字符串或正则表达式



####    去空 去掉字符串的空格 :
    var str = '   abcdef   ';
    console.log(qukong1(str));
	function qukong1(str){
		let reg = /^\s+ | \s+$/g; //去掉 开头+结尾的 空格
		let result = str.replace(reg,'');  //替换+去掉 开头空格
		//把检测到的空格替换为空  '  ' --> ''.
		return result;
	}
####   trim 去空格 :
	String.prototype.trims = function(type = 'l'){
	    let reg;
	    if(type == 'l'){        // left
	        reg = /^\s+/ ;
		}else if(type == 'r'){  // right
            reg = /\s+$/ ;
		}else if(type == 'a'){  // all
            reg = /^\s+ | \s+$/g ;
		}
		return this.replace(reg,'');
	};
	var str = '   abcdef   ';
	let result = str.trims('a');
	console.log(result);*/


	var reg = /\+/;  //转义字符 '\'  反斜杠  去掉\
	var str = '.a+\\bcd';
	let result = reg.exec(str);
	console.log(result);

###		屏蔽关键词
	var reg = /烂透了|死孩子|滚/g;
	var str = '死孩子真的是烂透了，出去';
	let result = str.replace(reg,'*****');
	console.log(result)  //输出  *****真的是*****，出去

###	 ？ 问号  最多出现一次，要么不出现
###  小括号 ()
	var reg =/ab(cd)?|ef/g;               //选择性的匹配
	//匹配结果:  ab  abcd   ef   如果有abcd，则先匹配abcd，否则ab
	var str = 'abcdef';
	console.log(reg.exec(str));  //  abcd
	console.log(reg.exec(str));  //  ef
	console.log(reg.exec(str));  //  null


	var reg = /[a-z]{3}(\d{3})/g;
	var str = 'asd123fghj456jkl789';
//	把数字也输出来。  对内容进行分组
	console.log(reg.exec(str));  //  ["asd123", "123",
	console.log(reg.exec(str));  //  ["asd123", "123",
	console.log(reg.exec(str));  //	["jkl789"，"789"


//获取字符串中 ''中的内容   ??????????????????????????????????????????????
	var str = "ab'cd'e'f'";			
	var reg = /[',"][^',"]+[',"]/g;  
	console.log(reg.exec(str))
	console.log(reg.exec(str))


	var str = "ab'cd'e'f'";
	var reg = /([',"])([^',"]+)\1/g; //反向引用  应用第一组内容  【[',"]】   小括号分组
//		   组号： 1组    2组     引用1组
	console.log(reg.exec(str))
	console.log(reg.exec(str))


	var str = "ab'cd'e'f'";
	var reg = /(:?[',"])([^',"]+)\1/g; //取消反向引用  应用第一组内容  【[',"]】   小括号分组
	//		   取消反向引用第一组
	console.log(reg.exec(str))
	console.log(reg.exec(str))


	var reg = /([a-z]+)-\1/;
	console.log(reg.exec('a-b'));
	console.log(reg.exec('ab-ab'));  //ab-ab
	console.log(reg.exec('ac-cb'))   //c-c
```



















