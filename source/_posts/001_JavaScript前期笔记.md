
---
title: 001_javascript前期笔记
---


##  Javascript 

``` bash
####★技巧★   鼠标移入手势
CSS中加入：
cursor: pointer;

####★技巧★
push 删除空格  
 if(arr[i]!=undefined){}

####★技巧★
数据类型  小写   number   

Hbuilder  改主题颜色
工具--视觉主题设置--夜间模式

####★技巧★
不同的script之间是有联系的

####★技巧★
可以引入其他格式文件
* `<script src="笔记.txt"></script>`

####★技巧★
给数据加引号‘’  双引号“”  ，选中加引号

####★技巧★
var min=[];   //数组需要设置  =[]  ，否则为undefined
> 数组的下标从0开始

#### ★技巧★
	弹框中输入数据
	var score=prompt('请输入您的分数','');
*	prompt('输入月份','');  //输入的都是字符型 <br>
	document.write('<b' 'r>'); //换行  
	
#### ★技巧★
	location.reload();//自动刷新页面   

#### ★技巧★
	html 标签中的叫属性，CSS里的设置叫样式
	


#★★★★★★★★20170418★★★★★★★★★

## JavaScript:        简称:JS

* ★组成★
1.ECMAScript
	+ 基础语法   变量   数据类型   运算符   结构   函数   对象   
2.BOM（browser object module）   浏览器对象模型
	+ window 子对象  导航
3.DOM（document object module）   文档对象模型
	+ html元素 属性 方法 样式 
	


## ★语法特点★
* 1.基于对象-和-事件驱动-的-松散型-的-解释性语言****
>	松散型:	数据类型  var a=1；
		 	句末是否加“；”分号
》	解释性：浏览器来解析
* 2.弱类型语言. 
* 3.XHtml



##引入方式
	* script 标签对
	* 外部js文件
	* 重定向
	* 超链接
	
>外部js文件中不能出现js标签对，script标签对中不能出现js代码：
	<a href="javascript:;">链接</a>    //a标签不会刷新
	

* 1.--在域名或重定向当中调用-<br>
	`<a href="javascript:alert(1)">链接</a>
	<form action="javascript:alert(2)">
		<input type="submit" name="" id="" value="" />
	</form>`
* 2.--在事件的后面调用-->
	`<div onclick="alert(3)"></div>`
* 3.--嵌入样式-->
    `<script>
    	alert(4);
    </script>`
* 4.--引入样式-->
	`<script src="js/demo1.js"></script>`


## 调试工具
	1. alert(1)  警示框
	2. document.write("123");    页面输出
	3. console.log("uek");      /*输出到控制台*/
	4. console.dir()
	5. alert(typeof arguments[1]);



## js干什么
* 数据验证
* 添加事件
* 操作dom对象 内容 样式  属性  
* 动画
* cookies
* ajax
* ...




##变量     ★声明变量★
>  存储数据的容器

###★声明变量★

> 'var 变量名'<br>
>  let c=3;  //JS的严格模式

	Example:
	'use strict';
	let hello = 'hello world.';
	console.log(hello);

 var 变量名=变量值;

####★变量名★
* 数字  字母  _ $  ,数字不能开头

> a12	a1a  _a  _$  $a  $1

* 关键字和保留字不能作为变量名
* 严格区分大小写
* 首字母大写 Object Array String
* 驼峰命名法   首字母大写
	>>getElementsByTagName()
* ;分号可加可不加

##### 第一种方式   声明的同时进行赋值
    var 变量=值  'var aa=1；'
   
##### 第二种方式   先声明后赋值
	var 变量；变量=值；
	var bb;
	bb="2";
	alert(bb)
	
##### 第三种方式  一次性声明多个变量之后进行赋值
	var name,age,sex;
	name="caoyue";
	age=33;
	sex="man";
	alert(age,sex);
	
##### 第四种方式 一次性声明多个变量同时进行赋值
	var name="xioaming",age=17,sex="man";
	alert(sex)
	
##### 直接调用一个未声明变量
	报错  变量未声明
##### 赋值之前进行调用，不给赋值
	默认值 undefined
##### 变量覆盖
	bb=2;  /*全局变量*/
	undefined;  /*声明未定义*/
	
	<script>		
    	var a=2;	
    	console.log(a)   //输出2
    	var a;		
    	console.log(a)   //输出2  因为第一次已经赋值，第二次没赋值
    	var a=5;	
    	console.log(a)   //输出5
    </script>	




=====================================

#★★数据类型★★★★★★0418★★★★★★★★★
* 栈：容量小，速度快。简单数据，用于快速读取。存放初始数据类型
* 堆：容量大，速度小。容量大的数据。存放引用数据类型


>number string  boolean undefined Object

###### 检测、判断数据类型 typeof

	var val="uek";
	alert(typeof val);
	var num=Number.MAX_VALUE;
	alert(num);
	var min = Number.MIN_VALUE;
	alert(min);
   	var val={name:"zhangsan"};
	alert(val);


### 1.初始类型
*	<1>数值  Number
>	数字/0/负数/八进制 011《会转化为十进制数显示》/十六进制0X11 / 科学计数法

012  输出10
018  输出18   因为是八进制最大是7，超过7就是十进制
*	<2>字符串  String

	双引号和单引号效果一样，允许相互嵌套
	特殊字符   \n \r \t \\ \b  &nbsp;&nbsp;&nbsp;第一个"\"为转义
>	用"" '' 双引号或单引号中的值.
	
*	<3>undefined
>	未赋值

*	<4>bull
>	‘true  false’ ***boolean***

*	<5>null   占位符
>	'null'    ***object***

### 2.引用类型    object
	包含属性和方法的集合
		对象
		原生
		数组
		函数

静态区：放常量

#★★运算符★★★★★★20170419★★★★★★★★★

 概念：
*	表达式：操作数和运算符的组合；有结果的语句。

### 1.算数运算符
	+ - * / %取余   ++自加   --自减
*   '%' 取余一般用于取一段范围的值
*	‘+’可用于字符串的拼接	、连接(字符串可以和任意的数据类型相加，相加结果为新的字符串)
*	模板字符串  ${字符串变量}
*	i++ 先运算后自增 ， ++i 先自增后运算
*	i++ 返回原来的值，++i 返回加1后的值。
#######Example
	var a = "10";
	var b = 4;
		var res = a+b;
		alert(res)     //输出104
		alert(typeof res)    //输出string
	
	var a = "10";
	var b = 4;
		var res = a+b-4;
		alert(res)     //输出100
		alert(typeof res)   //number
	
	var a = "10";
	var b = 4;
		var res = b-4+a;
		alert(res)     //输出010
		alert(typeof res)   //string
	
	var a = 37;
	var b = 33;
		var str='WUIF1702-1班有'+a+'人'
		alert(str)     //输出WUIF1702-1班有37人
		alert(typeof str)   //string
			
	模板字符串  ${字符串变量}
	var a = 37,b = 33;
	var str1=`WUIF1702班有${a}人`;
		alert(str1)     //输出WUIF1702-1班有37人
		
###### 字符串和其他类型相+时为连接的效果
	var str1="hellow ";
	var str2=123;
	var str3=str1+str2; //连接
		alert(str3);
		alert(str1%7); 取余

	i++ 返回原来的值，++i 返回加1后的值。
	var n=1;
	var n2=++n;
		alert(n2);
	
	++n=2
	n++=1		

	var num=22;
		alert(num++);   //22
		alert(++num);	//24
		alert(--num);	//23
		alert(num--);	//23
		alert(num);		//22
		alert(++11);	//错误   不能进行加减操作。num是个自变量，不能是定值
### 2.关系运算符(比较运算符)   
	> < >= <= ==相等   !=不等   !==   ===
*	运算结果为bull值：true false
*	‘==’ 比较数值
*	‘===’全等，比较数值和数据类型
##### 比较规则
*	两个数比较
*	两个字符型字符串。	会
*	成ACSII码比较
*   'b'<'bc' 两个依次比较，直到第一个不一样的值的大小
*	两个数字型字符串。       会转换成ACSII码比较
*	数字型和字符串比较。    会尝试把字符串转换为数字型，若转换不成，返回NaN (not a number),表达式结果为false.
+	"zumu" 引号里是字母的话，不能转换成数字,不能比较，“123”引号里是数字的话可以转换成数字，可以比较。
*	undefined == null (true)
*	undefined === null (false)
*	布尔值和数字，把布尔值转换成数字，true(1)  false(0)
######Example
	var num1="20",num2="5";
		var res=num1>num2;
		alert(res);   //false
	
	var num1="-20";
		var num2=5;
		var res=num1>num2;
		alert(res);   //false     ????????????????????
	
	var num1="-20";
		var num2=5;
		var res=num1<num2;
		alert(res);   //true    ??????????????????????? 
		
	alert(true == 1); //true
		alert(true === 1);//false
		alert(false == 0);//true
		alert(false === 0);//false
		alert("true" == 1);//false
		alert("true" === 1);//false
		alert( undefined == null);//true
		alert( undefined === null);//false
		alert( 'undefined' == 'null');//false
		
	var n1="a";
		var n2="c";
		var result=n1>n2;
		alert(result)
		字符以第一个字母的ACSII值比较
		A 65    a  96    0  48 

### 3.赋值运算符
	= += -+ *= /= %=
	var aa=10;
	aa+=1; 
	alert(aa)   //输出是 aa=aa+1  11 
### 4.逻辑运算符
*	&&(and)与       ||(or)或        !(not)非
*	与运算，整个表达式的结果为真，其结果为最后一个表达式的值
*	                 若表达式的结果为假，其结果为第一个假的表达式的值
*	undefined	false
*	逻辑运算符可以对任意的数据类型进行运算，在运算的工程中，转化对应的布尔值
*	undefined	null	0	空字符“”	    false  NaN
######  && 与
	var result=!false;
	var a=10;
		var b=20;
		var res= a<b && ++a;   //输出11 
		alert(res);
	表达式的结果为真，其结果为最后一个表达式的值
	var res= undefined && ++a;   //输出undefined 
	表达式的结果为假，其结果为第一个假的表达式的值
	var res= {} && ++a;   //输出11   {}为对象
	var res= {} && 0;   //输出0   0为假值，输出第一个假值	
######  || 或  or
	var a=10;
	var b=20;
	alert( a>b || b<a || a ); //10
### 5.一元运算符
*	typeof
*	‘+ -’  正号  负号
*	delete    删除对象的方法或属性
*	new 	创建对象
### 6.三元运算符
	根据表达式的结果，选择性的给变量赋值
	var aa=15;
	var bb=aa>10?aa:5

### 7.特殊运算符
	,  一次声明多个变量
	()  在运算的时候有优先级的作用
		让函数运行
	var num1=(10+10)*10;


#★0419★★流程控制★★★★★★★★★★★★★★★★★★

	流程：执行代码的顺序
### 1.顺序结构
	-按照书写顺序来执行
### 2.选择结构
	-根据给定的条件有选择的执行响应的条件语句
######	<1>分支结构
	注意if  else的顺序

*		单路分支  if(条件){条件成立执行}
*		双路分支 if(条件){条件成立执行}else{条件不成立执行}
*		多路分支 if
*		嵌套分支（满足条件不可以有重复的部分，会发生未知错误）

###### 如果判断条件是范围，优先用if else ,条件是单个值，优先用switch
		var aa=1234;
		if(aa<10){
			alert("1")
		}else if(aa>=10&&aa<20){
			alert("2")
		}else{
			if(typeof aa=="number" ) {
				alert("其他")
			}
		}

*	<2>条件结构

		var bb=3;
		switch(bb){
			case 1:alert("第一种");
			break;
			case 2:alert("第二种");
			break;
			default:alert("其他")
		}

### 3.循环结构
*	for一般用于循环指定的次数
*	while是根据条件的增加来循环，当真的时候进行循环，假的时候退出循环
*	跳转语句：break  
*	
*	
*	continue 
######  break
	document.write('hahaha<br>')
	aa:for(var i=0;i<5;i++){
		if(i==2){
			break aa;
		}
		document.write(i); //输出01
	}
	
	document.write('hahaha<br>')
	aa:for(var i=0;i<5;i++){
		for(var j=0;j<6;j++){
			if(j==2){
				break;
				//输出01  01   01   01   01   01
    		}
    		document.write(j); 
		}
		document.write('<br>'); 
	}
######  continue
	document.write('hahaha<br>')
	aa:for(var i=0;i<5;i++){
		if(i==2){
			continue aa; //跳过 2,继续执行后边的。最后输出0134
		}
		document.write(i)
	}

	document.write('hahaha<br>')
	aa:for(var i=0;i<5;i++){
		for(var j=0;j<6;j++){
			if(j==2){
				continue aa;
				//输出01 0101 01 01 01
    		}
    		document.write(j); 
		}
		document.write('<br>'); 
	}
######  for  满足给定条件下重复执行某一段代码

	'for(条件初始化；终止条件；步进值){循环体}'
	for(var i=0;i<10;i++){
		console.log(1)
	//		alert(i);
	}
	
######	  奇数增  偶数增

	for(var i=1;i<=10;i+=2){
			alert(i);
		}

######	 倒三角
		for(var i=1;i<=20;i++){
			for(var j=10;j>=i+1;j--){
				document.write("*");
			}
			document.write('<br>'); //换行
		}

######	 九九乘法表
		for(var i=1;i<=10;i++){
			for(var j=1;j<=i;j++){
				document.write(i+'*'+j+'&nbsp;&nbsp;&nbsp;');
	//			document.write(`${i}*${j}=${i*j};   `)
			}
			document.write('<br>'); //换行
		}
######	 while  先判断后执行
	var aa=10;
	while(aa<20){
		console.log(aa);
		aa++;
	}
######	 while if  循环+判断 
	var aa=10;
	while(aa<20){
		aa++;
		if(aa==15){
	//			break;
			continue;
			//当aa=15时终止当前循环，继续执行下一次循环。
		}
		console.log(aa);
	}
######	 do  while
	do{
	 	alert('do');
	 	a++;
	 }
	 while(a<12);


## ★0419★★★★★★★★★★数组★★★★★★★
*	存储一组或一系列相关数据的容器
*	数组的下标从0开始
*	空元素		arr[i]=undefined
*	空数组  		arr.push()
######	空数组    push
	var arr=[1,2,5,,"a","d",,"s"]
	var newarr=[];
	for(var i=0;i<arr.length;i++){
		if(arr[i]!=undefined){
			newarr.push(arr[i]);
		}
	}
	document.write(newarr)
#####删除数组里面的空值	
	var arr=[1,3,23,43,,23,3,,4,32,,43,,3,43,,,,,,,23]
		var arr1=[];
		var j=0;
		document.write('原数组为：&nbsp;'+arr);
		document.write('<br>原长度为：&nbsp;'+arr.length);
		for(var i=0;i<arr.length;i++){
			if(arr[i]!=undefined){
				arr1[j]=arr[i];
				j++;
			}
		}
		document.write('<br><br>数组为：&nbsp;'+arr1);
		document.write('<br>长度为：&nbsp;'+arr1.length);
		
####数组声明
	`var arr=[]`//空数组

	var arr=[];
	arr[0]=10;
	arr[1]=13;
	arr[2]=41;
	alert(arr)

	//Array 数组的构造函数
	var arr2=new Array(1,2,3);
	alert(arr2)

	var arr2=new Array();
	arr2[0] = 90;
	arr2[1] = 91;
	arr2[2] = 92;
	alert(arr2)
#### 数组 赋值
*	声明的同时进行赋值
	`var arr=[10,15,20]`
*	先声明后赋值
	`var arr=[]; 
	arr[0]=1; 
	arr[1]=2;`
#### 数组 访问
*	下标访问。下标从0开始。
#### 数组长度      arr.length

#### 数组遍历
*	for  
*	while
#### ◇数组◇
console.log(arr2)
console.dir(arr2)   //显示数组细节
alert(arr2.length)  //输出数组长度
#### 注意
*	 数组的长度是可变的 
*	可存储任意的数据类型
*	数组元素如果没有值，默认undefined
*	数组长度是可变的

##### 可存储任意的数据类型
	var arr3=["uek",1,undefined,true,null,function(){},arr2]
	alert(arr3)

##### 练习1：数组最大最小值
	var arr=[90,20,80,113,4,3,54,34,89];
	var max=arr[0];
	for(var i=0;i<=arr.length-1;i++){
		if(arr[i]>max){
			max=arr[i]
		}
	}
	alert(max)
##### 练习2. 冒泡排序
	/*
	arr=[90,20,80,113,4,3,54];
	
	1. min=arr[0];
	   90 20 80 113 4 3 54
	   20 90 80 113 4 3 54
	   
	2. min=arr[1]
	   20 90 80 113 4 3 54
	   20 80 90 113 4 3 54
	*/
		var arr=[7,13,76,34,9,23,65,2];
		for(var i=0;i<arr.length;i++){
			for(var j=i+1;j<arr.length;j++){
				if(arr[i]>arr[j]){
					var flag=arr[i];
					arr[i]=arr[j];
					arr[j]=flag;
			//		arr[j]=arr[i]+arr[j];
			//		arr[i]=arr[j]-arr[i];
			//		arr[j]=arr[j]-arr[i];
				}
			}
		}
		document.write(arr)


#### ◇数组◇
var arr2=new Array(4);
//	console.log(arr2)
	console.dir(arr2)   //显示数组细节
	输出为 [undefined,undefined,undefined,undefined]
	在数组实例化的时候,如果只传递一个参数的话,这个参数表示数组的长度.新数组的长度是可变的,随着参数的变化而变化

#### 查找数组里的第i行的第j个值
     for   while   for in
   
	var arr4=[[1,2,3],[4,5,6],[7,8,9]];
	
	for(var i = 0; i < arr4.length; i++){
		for(var j = 0; j < arr4[i].length; j++){
			console.log(arr4[i][j])    //数组里的第i个的第j个值
		}
	}

#######取得二维度数组中长度最大的数组	
	var arr=[[1],[2,3,4],[42,34,432,32,234,432,234],[1,12,12,21,23]];
	var max=0;
	var flag=[];
	for(var i=0;i<arr.length;i++){
		if(max<arr[i].length){
			max=arr[i].length;
			flag=arr[i];
		}
	}
	document.write('长度最大的数组为：&nbsp;'+flag);
	document.write('<br>最大长度为：&nbsp;'+max);



#★★★★★★★★20170420★★★★★★★★★
#表格
	var table='';
		table+='<table border=1 >';
    	for(var i=0;i<6;i++){
    		table+='<tr>';
    		for(var j=0;j<6;j++){
    			table+='<td>';
    			table+=j;
    			table+='</td>';
    		}
    		table+='</tr>';
    	}
    	table+='</table>';
    	document.write(table);
    	
	表格方法2
    	document.write('<table border=1>' );
    	for(var i=0;i<5;i++){
    		document.write('<tr>'+i);
        	for(var j=0;j<6;j++){
        		document.write('<td>'+j+'</td>');
        	}
        	document.write('</tr>');
    	}
    	document.write('</table>');


## ★0420★★★★★★★★★★函数★★★★★★★
将实现某一特定功能的代码集合起来重复调用的代码块

# ★函数★
	将一段特定功能的代码块封装起来重复调用
*	调用函数需要写函数名的括号 "()" 
*	后边声明的函数会覆盖之前的
*	字面量函数必须在后面调用


#### ◆函数声明◆
	1.基本语法<br>
	function fnName([参数1]，[参数2],...){
		函数体
		[return 返回值;]
	}

	2.字面量方式
	var 变量名([参数1]，[参数2],...){
		函数体 
		[return 返回值;]
	}

	3.//实例化对象的
	var	funobj=new Function();

#### ◆函数调用◆
	1.val();
	2.在事件只有之后调用
	3.函数 自调用:在函数外加个小括号
	(function fun(){})();
*	调用注意：
函数名相同时，后面的函数会覆盖前面的函数
*	一基本语法声明的函数
####先定义后调用
*	在不同的`<script></script>`中浏览器按照从上到下的顺序进行解析，后面的代码块可以调用前面的函数，前面的代码块不能调用后面的 函数

######基本语法   *弹出1*    可以在前面调用 
	tan1();
	function tan1(){
		alert(1);
	}
	tan1(); 

######字面量方式    必须在函数后面调用
	var tan2=function(){
		alert(2);
	}
	tan2();

	var tan1=function(){
		alert(1);
	}
	tan1(); //输出1

	var tan1=function(){
		alert(2)
	}
	tan1();//输出2


#### ◆运行函数◆
函数名
*	table()

变量名
*	table()

自调用	
*	`(function(){}){}`

#### ◆函数的参数◆
>	考虑 参数、几个参数、参数类型、要不要给默认值

*	形参  	声明的时候。接受实参传递的值
*	形参参数名不能相同
*	实参		调用的时候。给形参传递值
*	tan(1,,4) 错误！！    函数参数不能为空    
*	tan(1,undefinned,4)		函数不会报错  输出若有默认值，会代替undefined。
*	tan(undefined,null,4)	输出 undefined null 3 ,null不会被替换，    
*	tan(1,2,,)    空格在最后
*	function tan(a,b,c=5) { //形参带默认值的会默认放在最后 c=5 放在最后}
*	
*	默认值num===undefined?'zhangsan':num;


######	rest
	// REST函数  rest参数
	function addnum(...values){  //将值打包给values
		document.write(values);
	}

	function addnum(a,...values){ //将没有值打包给values
		document.write(values);
	}

######	参数重载


####	参数初始化的方法
	1. if
	2. 三元化    num= num===undefined ?'zhangsan':num;
	3. num= num?num:'zhangsan';
	4. num= num || 'zhangsan';
	5. function tan(num='zhangsan'){
			document.write(num);
		}

*	function tan(num='zahngsan'){
			num==num?num:'zhangsan'
			document.write(num)
		}
		tan(2)

######  形参 返回值
	function sum(num1,num2){//形参
		num3=num1+num2;
		return num3;
	}
	var result=sum(10,11);
	alert(result);

	function tan(num){
		alert(num);
	}
	tan(5);		//弹出5
	tan(9);		//弹出9	
	
####### 写表格    注意 table 声明 var	 
	//  弹出框
	function table(rows,cols){
		var table='';
		table+='<table border=1>';
		for(var i=0;i<rows;i++){
			table+='<tr>';
			for(var j=0;j<cols;j++){
				table+='<td>'+j+'</td>';
			}
			table+='</tr>';
		}
		table+='</table><br>';
		document.write(table);
	}
	table(1,2);
	table(5,5);
	table(9,9);

#### ◆type 检测参数的类型◆
	function type(i){
		if(typeof i =='number'){
			document.write('number');
		}else if(typeof i=='string'){
			document.write('string');
		}else{
			document.write('其他')
		}
	}
	type(null);
	type(2);
	type('a')

####  pushadd  给某一个数组在他的最后添加一个元素
	ele  永远是个数组，当没数时为空数组
	/*function pushadd(arr,ele){
		arr[arr.length]=ele;  
		document.write(arr);
	}*/   
	
	function pushadd(arr,...ele){
		for(var i=0;i<ele.length;i++){
			arr[arr.length]=ele[i];
		}
		document.write(arr);
	}

##### ★模拟函数重载★
	同一个函数因为参数的类型或数量不同，可以对应多个函数的实现，每种实现对应一个函数体
	//  求1-10的累加和
	function fun(){
		if(arguments.length == 1){
			var sum=0;
			for (var i = 0; i <= arguments[0]; i++){
				sum+=i;
			};
	//			return sum;
		}else if(arguments.length == 2){
			return arguments[0]+arguments[1]
		}
	}
	var num=fun(60,40)
	alert(num)

####  ◆arguments 对象◆
	console.log(arguments);    //以数组形式输出
	alert(arguments.length);   //输出实参的个数
	alert(arguments.callee)    //输出function    获取函数本身
	alert(typeof(arguments[1]));   //数组类型

*	实参比形参多    arguments
*	形参比实参多    undefined

##### ★return★   返回值
*	函数默认值  undefined
*	可以是任意的数据类型，只能返回一个值
*	终止函数运行
*	函数体内部可以有多个return，但只执行一个    在分支语句中
	
##### eg:第一步就判断  返回
	`function num(ele){
		if(typeof ele != 'number'){
			return 7;
		}
		if(ele%2==0){
			return '偶数';
		}else{
			return '奇数';
		}
	}`
	num(1);
	document.write(num(1))
	
	//返回任意数据类型
	function aa(ele){
		console.log(ele);
		//return ele;  //可以返回任意数据类型   没有return的话，ele的值只能看，不能用
	}
	var a=aa(1);
	console.log(a);
	
	//只允许返回一个值   返回c
	/*function aa(ele){
		console.log(ele);
		return ele;}
	var a=aa(aa);       //返回函数运行
	console.log(a);*/
	
	function aa(ele){
		console.log(ele);
		return 'a','b','c';  //只允许返回一个值   返回c
	}
	var a=aa(1);
	console.log(a);


### ★0421★★★★★★★★★★函数★★★★★★★

######  判断  push 是不是数组
	if(push instanceof Array){  //判断    push 是不是数组 }

######	+ - * / 运算
	function calc(num1,num2,ysf){
		if(ysf=='+'){
			return num1+num2;
		}else if(ysf=='-'){
			return num1-num2;
		}else if(ysf=='*'){
			return num1*num2;
		}else if(ysf=='/'){
			return num1/num2;
		}
	}
	var a=calc(2,4,'/');
	document.write(a);

######	回调函数      通过函数的指针来调用函数
	一个函数作为另一个函数的参数（形参）调用
	function math(num3,num4,fn){
		return fn(num3,num4);
	}
	
	function aa(num1,num2){
		return num1+num2;
	}
	function bb(num1,num2){
		return num1-num2;
	}
	function cc(num1,num2){
		return num1*num2;
	}
	function dd(num1,num2){
		return num1/num2;
	}
	
	var b=math(7,2,cc);
    document.write(b);

######	箭头函数   ES6 新加的
	var s2=ele => ele;
	//  函数名=形参=>返回值；
	var s3=s2(123);
	document.write(s3+'<br>');
			
	var s2=(ele1,ele2) => {return ele1+ele2};
	//  函数名=形参=>返回值；
	var s3=s2(123,1);
	document.write(s3+'<br>');
	
	var aa=function(ele){
		return ele;
	}
	var resule=aa('a');
	var dd= (ele,ele1) => 'a1';
	var ee= (ele,ele1) => {return ele+ele1};
	var ff=(ele,ele1) => {alert(arguments.length)};
	alert(ee(1,2))

######	递归函数
	function down(num){
		if(num<=0){
			return num;
		}
		document.write(num+'<br>');
		down(--num);
	}
	down(10)

######	递归阶层
	function jc(num){
		if(num==1){
			return 1;
		}else{
			return num*jc(--num);
		}
	}
	var val=jc(5);
	document.write(val+'<br>');

#### 视频.函数高级用法
	<3>闭包函数
		function aa(){
			var num=10;
			function bb(){   //闭包函数
				num++;
				return num;
			}
			return bb;
		}
		var val = aa();
		alert(val())
		alert(val())
		alert(val())
外层函数调用内层函数的局部变量

## ★★★作用域★★★★★★20170421★★★★★★★

#### 环境
*	宿主环境
*	执行环境
	+ 全局变量
	+ 局部变量
*	形参属于局部变量


#### 1.变量的作用域
	<1>全局变量
	<2>局部变量
		num = 5;	 //全局变量 
		var val1 = 10;   //全局变量
		function fun3(){
			var val2 = 20;   //局部变量
			function inner(){  //局部函数变量
				alert(1);
			}
			inner();
		}
		fun3();
	<3>作用域链
		var val1 = 10;   //全局变量
		function fun3(){   
			var val1 = 20;   //局部变量
			alert(val1)
		}
		fun3()

	var b=1;
		function aa(){
			document.write(b);   //输出  undefined
			var b=2;
			document.write(b);   //输出  2
		}
		aa();
		document.write(b);   //输出  1

	var b=1;
    	function aa(){
    		document.write(b);   //输出  2
    		b=2;
    		document.write(b);   //输出  2
    	}
    	aa();
    	document.write(b);   //输出  1

		var b=1;
        	aa();
        	document.write('这是1--'+b+'<br>');
        	
        	function aa(){
        		document.write('这是2--'+b+'<br>');
        		var b=2;
        		document.write('这是3--'+b+'<br>');
        	}
        	输出:
	        	这是2--undefined //里面有b，只是没赋值，所以为undefined
				这是3--2
				这是1--1


		var b=1;
        	aa();
        	document.write('这是1--'+b+'<br>');   
        	function aa(){
        		document.write('这是2--'+b+'<br>');  
        		var b=2;
        		document.write('这是3--'+b+'<br>');   
        		bb();
        		function bb(){
        			document.write('这是4--'+b+'<br>');
        			b=3;
        			document.write('这是5--'+b+'<br>');
        		}
        	}
        	输出:
	        	这是2--undefined
				这是3--2
				这是4--2
				这是5--3
				这是1--1


##  let
	document.write('这是--'+a+'<br>');
	{
		var a=1;
		let b=2;
	}
	document.write('这是--'+a+'<br>');
	//输出：
	这是--undefined
	这是--1









# ★内置顶层函数★
*	顶层函数:拥有全局作用域的
*	内置:直接调用,不用声明


# ★数据类型转换★
1.Number() 转换成数值类型
2.String() 转换成字符串类型
3.Boolean() 转换成布尔类型
4.parseInt() 将字符串转换为整型
5.parseFloat() 转换为浮点型

#####// Number 转换成数值类型			
	//	E.如果是字符串		
	//	1.如果字符串当中只有数字，转换为10进制(忽略前导0和后导0)
	//	2.如果是有效的规范的浮点型，转换为浮点值(忽略前导0和后导0) 
	//	3.如果是空字符串，则转换为0    
	//	4.如果是其他的值，返回NaN
	document.write(Number(012)+'<br>');			//	10		八进制
	document.write(Number('012ABC')+'<br>');    //	NaN  
	document.write(Number('012')+'<br>');		//  12		数字,转换成为本身,无意义的后导0去掉
	document.write(Number('1234.000')+'<br>');	//	1234
	document.write(Number(' ')+'<br>');			//	0		null转换为0
	document.write(Number('1.2.3 ')+'<br>');	//  NaN
	document.write(Number('a2333')+'<br>');		//  NaN
	document.write(Number('undefined')+'<br><br>');	//	NaNundefined 转换为 NaN
	
#####// String  将任何的类型转换为字符串     加了个引号     
	//布尔类型:会返回true 和false		
	// 数值类型:本身的字符串				
	document.write(String('123')+'<br>');   //  123
	document.write(String('a2333')+'<br>');   //a2333
	document.write(String(undefined)+'<br>');
	document.write(String(null)+'<br><br>');
	
##### 布尔值   Boolean
	document.write(Boolean(null)+'<br><br>');   //真假  false  true
	//  ''  0  NaN   undefined   false  null     转化为假   其他都为真
        		
        		
##### 判断能否转换为数值类型        isNaN
	//	如果能转换成数值返回假，不能转换成数值类型，返回真
	document.write(isNaN(true)+'<br>');         //false
	document.write(isNaN('ABCD')+'<br><br>');   //true
	
#####//将字符串转换为整数    parseInt
	//A.如果一个字符串只包含数字，则以10进制的方式转换为整型
	//  开头必须是数字、空格
	document.write(parseInt('123hjk321')+'<br>');   //转换为数值类型   123
	document.write(parseInt('defau32')+'<br>'); 		//NaN
	document.write(parseInt(100,2)+'<br>'); 		//2进制  4
	document.write(parseInt(100,8)+'<br><br>'); 		//8进制  64
	var str="0x11";
	alert(parseInt(str));   //弹出17    进制解析
	
#####// 将字符串转换为浮点数   parseFloat
	//A.字符串当中的 . 只有第一个有效，其他的都是无效的。
	//B.如果字符串是一个有效的整数，他返回的是整数，不会返回浮点数。
	document.write(parseFloat('1.2.3')+'<br>');
	document.write(parseFloat('123acb'));




##练习：
##### 表格
	function table(){
		document.write('<table border=1 bgcolor=blue>');
		for(var i=0;i<6;i++){
			document.write('<tr>');
			for(var j=0;j<6;j++){
				document.write('<td>');
				document.write(j);
				document.write('</td>');
			}
			document.write('</tr>');
		}
		document.write('</table>')
	}
	table();






## ★0424★★★★★函数-隐式类型转换★★★★★★★
* 	1.运算符

	+	`- * / %`如果操作数不是数值，将会隐式的调用Number()函数，按	照这个函数的转换规则进行转换.
	+	如果转换不成功，整个表达式返回NaN
	+	`+`	如果操作数都是数值，然后进行相加任何数据类型和字符串相加，然后返回他们拼接的结果。
	+	如果操作数都布尔值，那么进行Number()转换，false为0，true为1，进行相加

###### eg:
	// 	var num='5';
    var num='5px'
	var num1=10;
	document.write(num-num1+'<br>'); //输出NaN

	var num='null'
	var num1=10;
	document.write(num-num1+'<br>'); //输出NaN

	var num=null;
	var num1=10;
	document.write(num-num1+'<br>'); //输出-10

	var num=true;
	var num1=10;
	document.write(num-num1+'<br>'); //输出-9

	var num='true';
	var num1=10;
	document.write(num-num1+'<br>'); //输出NaN

	document.write(+0 == -0);//输出true
	document.write('<br>');
	document.write(NaN == NaN);//输出false
	document.write('<br>');
	document.write(true == 1);//输出true
	document.write('<br>');

## let
*	不能重复定义
*	作用范围
*	嵌套
	{
		let a=10;
		{
			let a=20;
			console.log(a);
		}
		console.log(a);
	}
*	不存在变量提升，先声明后调用
*	暂时性死区   tdz
+	function aa(y=x,x=2){}
+	function aa(x=x){}
+	形参不能用let重新声明
#####	块级作用域
		{	}
	let=b
	let 允许重新赋值,但不能重新声明,会报错.
	let 只在块儿中起作用

	{
		var a=10;
		let b=20;//只在块儿中起作用
	//	document.write(b);
	}//大括号--代码块
	document.write(a);//在括号里一样
	document.write(b);//无法输出，报错。只在块儿中起作用

	function aa(num){
		//let num=20;//报错   num已经声明，不能重新声明
		num=20;//正确
		document.write(num);
	}
	aa();

#####  不合理
*	变量提升
*	for循环下标i泄露
*	let 记录当前循环下表 i
-	for
	????????????????????????????????????????????????????????????????
######变量的提升
        	{
    //temporal dead zone 暂时性死区
        		document.write(a);//not defined    暂时性死区
      	//		var a=1;
        		let a=10;
        		document.write(a);
        	}

	*隐式性的暂时性死区
	function aa(z=z){
		num=20;
		document.write(z);
	}
	aa();//会报错


	let a='a';
	{
		let a=10;
		{
			let a=20;
			document.write(a);	//20
		}
		document.write(a);		//10
	}
	document.write(a);			//a

#####	for循环下标i泄露
	* let
	var arr=[];
	for(var i=0;i<10;i++){
		arr[i]=function(){
			document.write(i);
		}
	}
	arr[6]();    // var 声明 输出10。执行调用的时候，for循环已经跑完了，所以为10.
				// 	let声明 输出6


	var arr=[];
	for(let i=0;i<10;i++){
		arr[i]=function(){
			document.write(i);
		}
	}
	arr[0]();   //输出0  for循环每次循环都会记录下.
	arr[3](); 	//3		存下了i的值
	arr[6](); 	//6
	arr[8](); 	//8


	function aa(z=y,y=x){
		document.write(z,y);
	}
	aa(1,2);//输出  1  2



##	隐式数据类型转换
	四则元算
	关系运算符
	逻辑
	语句
	if()
	while()
	boolean espression?真：假；


















# ★★★★★★★★★★★★★对象★★★★★★★★★★★★★★★★★★★
*	属性和方法的无序集合体 当属性值为函数的时候 我们把这个属性称为对象的方法
*	instanceof  判断是否为对象 	alert(
*	one instanceof Object);
#####  声明对象
	class里是在constructor里写this，function里是直接写.
	可以加 person.prototype={  } 和json的写法相同。

		1.类名的方式
		class person{	};
		var zhangsan=new person();

		2.Json
		var 变量={属性名/属性值/方法(属性值为函数)}
		var zhangsan={};
		console.log(apple.tv == sanxing.tv);
		//false  tv是函数。两个函数比较时，比较的是地址，地址不同，所以是false
		console.log(apple.name == sanxing.name);//true


		3.构造函数
		function person(){	}
		var someone=new person();



		4. 内置顶层函数   new
		var someone3 = new Object();
		someone3.name='zhangsan';
		someone3.age=17;
		someone3.sex='man';
		someone3.say=function(){
			alert("shuohua")
		}
		someone3;

#### 3.类
	具有相同或者相似属性的对象的抽象描述就是类
*	类的具体化（实例化）就是对象
*	在javascript当中是通过构造函数来体现类的特性的

#### 4.实例化
	由一个抽象的概念得到具体的事物的过程
*	通过new构造函数

*	1.使用JOSN方式JavaScript的原生对象描述法
*	2.实例化构造函数
*	3.内置顶层函数

###### eg:
	1.类名的方式
	class里面属性、方法删不掉。
	class person{
		constructor(){  //属性值		构造函数
			this.age=18;
			this.name='lisi';
			this.drink1=function(){
				alert("干杯");
			}
		}
		play(){
			alert('这是方法');
		}
		study(){
			alert('学习的方法');
		}
	};
	let zhangsan=new person();
	zhangsan.tall='180cm';
	zhangsan.drink=function(){
		alert('喝酒伤身');
	}
	console.dir(zhangsan);
	console.log(zhangsan.tall);
	zhangsan.play();
	zhangsan.drink();
	zhangsan.drink1();


	2.Json方式
	let apple={
			brand:'apple',    //注意此地的逗号
			color:'red',
			size:750,
			call:function(){
				alert('打电话');
			}
		};
		apple.price=6500;
		console.dir(apple);
		console.log(apple.price);
		apple.call();
		
	3.构造函数方式
	function person(name,age,tall,say){
		this.name=name;
		this.age=age;
		this.tall=tall;
		this.say=function(){
			alert('shuohua');
		}
	}
	person.prototype={  //原型对象
		tizhong:180,
		play(){
			alert('玩儿');
		}
	}
	var someone=new person();
	console.log(someone.tizhong);
	someone.play();

3.编写一个构造函数，并通过new方式来创建对象，构造函数本可以带有构造参数 
	例如： 
	function User(name,age){ 
		this.name=name; 
		this.age=age; 
		this.canFly=false; 
	} 
var use=new User(); 


#####访问 :
	访问属性+方法
	访问值.属性
	访问值["属性"]
	仿问值.属性
	仿问值["属性"]();

	alert(apple.name);
	alert(apple['name']);   //括号当中必须是字符串
	apple.message();
	apple['message']();   //

#####遍历
		for(let i in apple){
			console.log(`属性${i}---${apple[i]}`);
	//		console.log(someone2[i]);//访问单个
		}

#####删除
	       json属性删除后是undefined
	delete someone2.name;

#####清空
	someone2=null;

``` 