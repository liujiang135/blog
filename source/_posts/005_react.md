---
title: 005-react
---
 
## React

```bash

"proxy": "http://jiangtoutiao.duapp.com/",
  "proxy": "http://localhost:80/",

#########   Route  就是路由

##############    react本地打不开，获取不到数据库。把那个重启   npm start     ################

git上传要写限制500M那个，要不页面不更新

#######################  REACT  中不允许用 == 两个等号  ####################################

###        const命令
const声明一个只读的常量。一旦声明，常量的值就不能改变。


###  报错    中间又函数没传过去
 _this3.props.onChange is not a function
中途所有传数据的  传的函数都要传
eg:	传3级
	<Index onChange={this.onchange} />
	<TopMenu data = {this.props.data} onChange={this.props.onChange}/>
	<a onClick={()=>this.props.onChange(v.id)}>{v.name}</a>

###  报错    Array to string conversion
echo和print 输出数组报错！echo 和print是输出字符串的。
请使用var_dump,print_r


###  报错  
数据库不要随便输出、

不要 echo  ok

或print_r data，有可能返回到ajax,不认识

###   一般项目开发可嵌入 react.js   css.js  文件来开发
   引入  react


###  浏览器  下载  sql 
直接 ctrl+s  保存为  .sql.txt   ，sql导入时直接导入就行  


###  
如果出现404页面 是路径问题   大小写问题

###   Error    Wraing
1.注意所有用到 db的地方  大小写
2.db 中的 public function query($spl) 没写
3.  db   28 47行
4.

    onclick(){
        $('')
    }

###    出不来页面：
/view/
改成APP/view/
进了php的 function index(){ 中，print_r(123); 看一下，能不能出来123.}
如果还是没有，看看 include 'APP/view/gameadmin.html'; 这几个字对了没，核对文件夹里，
是不是 gameadmin  写成 Gameadmin 了 。一般只有这个错误


###   git 组织

1.右上角 git  +  最后一个  新组织
2.创建新组织  账户 
3.添加好友账户
4.创建 文件 
5.设置每个用户是owner.大家就可以上传了。


## 注意单词拼错 导致报错

###  注意 super报错
class Logins extends React.Component   `不是ReactDOM `
ReactDOM.render(<Login/>,document.querySelector('#root'));

###  数组对象 集
console.table()

在 db 中加入



 3个JS 文件
bowerser.min.js
react-dom.js
react.js


###    home.html
    <script src="<?php echo JS_PATH?>browser.min.js"></script>
    <!-- 将ES6转成 ES5  加载完后会寻找 type="text/babel" 的文件，解析，由babel调用jsx的数据，拿回齐数据转换，执行-->
    <script src="<?php echo JS_PATH;?>react.js"></script>
    <script src="<?php echo JS_PATH;?>react-dom.js"></script>
    <script type="text/babel"  src="<?php echo JS_PATH;?>index.jsx"></script>


###    jsx文件
// 虚拟dom
//解决比对问题，让页面更高效
// render 渲染

var data = [1, 2, 3, 4];
var el = (
    <ul>
        {data.map((v, i) => <li key={i}>{v}</li>)}
    </ul>
);
ReactDOM.render(el, document.querySelector('#root'));

setTimeout( () =>{
var data = [1, 2];
el = (
    <ul>
        {data.map((v, i) => <li key={i}>{v}</li>)}
    </ul>
);
ReactDOM.render(el, document.querySelector('#root')); }, 3000);
//  render(虚拟dom对象,真实的DOM对象)   把虚拟dom转换为真实dom



#######################    20170713   #########################################
  
// 1. 虚拟DOM       //解决比对问题，让页面更高效
const el = <h1>this is h1</h1>;
// 2. 虚拟DOM 之 组件
// react.js     window.react
// react-dom.js   window.reactdom
// 3. 组件 -> state
// 4. 组件 -> props
// 5. 组件 -> 生命周期    componentDidMount
// 6. 组件 -> 事件系统
// 7. 多组件协作（如何拆分组件）


###   
eval('2+3*4')


################################33################################33##############################

####################################  安装react app 环境  ######################################33

################################33################################33#############################
npm install -g create-react-app   
切换到桌面
运行 create-react-app  test
漫长的下载过程
cd test
npm start


### 在 json语法中严格不能使用单引号
##  `网址`
https://reacttraining.com/react-router/web/example/basic


`注意错别字`

在： npm react  test里
package.json 里

npm install react-router-dom --save  `下载组件  Router Route Link`
npm install swiper --save  `下载组件  Router Route Link`
###  ***"proxy":"http://192.168.3.55:80",***

npm start

##### 引入jquery 
npm install jquery --save   `下载组件  jquery`
import $ from 'jquery';
npm start

`下载组件  antd zujian-------------------------///////////////////-----------------------////////`
npm install antd --save  

#################  #################

npm install wangeditor --save

###################     npm start之后有哪些工作        ###########

npm start
 1.启动了一个本地服务器(webpack - dev - server)   (以前是apache)，
 2.自动打开浏览器，访问服务器地址 localhost:3000/ 时
从index . js开始找到所有的 import 的资源
bludle . json_encode
......js

public/index.html   写入上一步生成的js和css路径
js. websockt serviceworker

检测src下的所有文件，有任何变化，
服务器用过websocket建立起来的长连接
通知浏览器 （浏览器收到通知以后刷新页面）

#############################################################
怎样上线：

npm run build

build/
    index.html
	xxx.js
	xxx.css
	img/.............


#########################################################################################

直接输入
`explorer http://www.baidu.com`
就会打开百度

 component={Search}

#########################################################################################
	antd 组件			https://ant.design/components/icon-cn/
########################################################################################
看代码 ，看示例，分析代码
##  Icon 去Icon图标里取找

##　 布局
##  table 表格
    columns   列     data  行

#########################################################################################
ES6  箭头函数
#########################################################################################
`
const {a,b,c,d} = {a:1,b:2,c:3,d:4}
const fn = (v)=>{console.log(v)}
const fn = (v)=>{
    return (
        <div>this is h1</div>
    )
};`

const fn = (v)=>（ v.id = id）

###  箭头函数
class Admin1 extends React.Component {
    constructor() {
        super();
        this.state = {
            a: 1,
            b: 2
        }
    }
    
    render() {

const {a,b,c,d} = {a:1,b:2,c:3,d:4}
        const fn = (v)=>{console.log(v)}
        const fn = (v)=>{
            return (
                <div>this is h1</div>
            )
        };`

        //解构赋值
        const {a, b} = this.state;
        // 对象展开
        const o = {x: 1, y: 2, z: 3 ,w:()=>{}};
        return (
            <div>
                <h1 {...o}>自定义属性</h1>
            </div>
        )
    }
}

##################################

改state，不要改props。

##########################################################################################
							phpstrom编程字体
consola
monaco
monosoace
source
menlo
consolas

vim 编辑

##########################################################################################

上传图片    

web-dev-server  服务器

在百度云申请服务器：

1.申请服务器
2.gitclone 
3. 复制框架：    app					home.php
									html      index.html
4.              core				db.php
5.              index.php
6.              public

用框架里的index.php替换掉这个clone下的index.php



4.创一个.gitignore文件    忽略某些    
在里面写`.idea/`  和文件的名字

5.git add上去

导出  database.sql    添加drop文件

放在主文件目录下

news 导出自定义 sql文件  

百度云数据库导入文件和数据库

修改db


script:public/js/bundle.js
home:index

###   npm run build
1.改public下的东西，static替换public
2.修改 /20170713/react/index.php/   改为  /  数据库路径



把 build 下的json\ico拷贝到根目录下

public  改为 static

重新git 

把后台出去
##########################################################################################
md5(time());

##########################  改进3部曲
1.改为： 
2.  - url : /
    script: index.php
  - url : /static/(.*)
    static_files : static/$1
  - regex_url : ^/(.*)$
    script : index.php/$1

2.页面拆分
  home.php-->index
  admin.php-->admin


	npm run build     之后    
3.替换
fetch("/index.php/
fetch("/

4.import router  和  router

####  后台的修改
5. 把后台生成的index.html名字改为admin.html，再放到百度云上传的文件中 
6. 把后台的css\js的东西放进去 


getNewsById  的limit的修改

####  改到百度云的 数据库
  "proxy": "http://localhost",
name:'text'


####   下拉刷新代码   下滑刷新
var neirong = document.querySelector('.contentall');
let that = this;
window.onscroll = function () {
    if (document.body.scrollTop >= neirong.offsetHeight - window.innerHeight) {
        var page = that.state.page + 1;
        console.log(page);
        fetch('/20170713/react/index.php/home/getNewsByPage?id=' + that.state.currentChannel + '&page=' + page)
            .then(res => res.json())
            .then(r => that.setState({
                o: that.state.o.concat(r),
                page:page
            }))
    }
}

###################        20170722     ###########################

<Route path="/show/:id" component={Show}/>  
{/*传入id*/}
show 组件中 iframe
网址中 /show/assdfghj   /show/后边所有的(assdfghj) 都会传到:id中去


上传图片到服务器
   把http:localhost80改为   /static/upload


  <div dangerouslySetInnerHTML={{__html:123}}></div>
```