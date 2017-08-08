---
title: 006- nodeJS
---


## nodeJS

```bash

###网址：         webpack.js.org
解决问题网址：  https://stackoverflow.com/

Buffer 是ES6新引入的数据类型

// Buffer 需要 先转成string
   Buffer通过toString()转成字符串


###★技巧★   explorer .   可以打开当前文件夹

打开浏览器：
child.spawnSync('explorer', [])  数组


###★技巧★   编辑器 let  箭头函数 报错
在设置中改为 ES6


### 基础知识   运行环境
1.Node.js 是一个基于 Chrome V8 引擎的 JavaScript `运行环境`。 
2.在 控制台 cmd中运行。是一种环境。



#######  1.   处理文件   node-module     ###############################
const os =require('os');  //  operation system 操作系统
const fs =require('fs');  //   file system  文件系统
const path =require('path');    //  path

const base =path.join(os.join(os.homdir(),'Desktop'));    //用户目录
for(var i =0;i<100;i++){
    fs.mkdirSync(path.join(base,String(Math.random())))
}

//make directory sync 创建一个 目录
//path.join 是连接路径

#######   下载request
npm install request
npm install cheerio
安装自动监测自动运行程序
npm install -g nodemon
npm node package manager


#######   运行  node index.js 执行程序
#######  安装自动监测后  nodemon index.js 执行程序

#######     2.    发起网络请求

const request = require('request');
const cheerio = require('cheerio');
request.get('http://www.baidu.com', (err, response, body) => {
    var $ = cheerio.load(body.toString());
var imgUrl = 'https:' + $('#lg').find('img').attr('src');
//buffer stream
request.get(imgUrl).pipe(
    fs.createWriteStream(
        path.join(__dirname, 'baidu-logo.png')
    )
)
})


//随口说出五个   request   cheerio  ...

#######   3.创建自己的node_modules 文件
建一个文件夹 eg:  get-bing-pic
控制台   npm init   -->  创建 package.json
一直回车


npm publish   //npm 发布

path.resolve('./'+'asd'+jpg')

npmjs 发布前要像搜索一下，不能发重复的



###         npm官网上传文件
node内建文件夹
cd +文件夹名
js中添加： #!/usr/bin/env node
npm init（一直回车） --》  创建packjson.json
npm install request --save
在node下创建index.js
index.js内编写此代码：
const request = require('request');
const path = require('path');
const fs = require('fs');
var getpic = (fn) => {
    request.get('https://cn.bing.com/HPImageArchive.aspx?format=js&idx=0&n=1&nc=1500903673140&pid=hp', (err, response, body) => {
        var url = JSON.parse(body.toString()).images[0].url;
        var name = JSON.parse(body.toString()).images[0].enddate;
        request.get('http://cn.bing.com/' + url).pipe(
            fs.createWriteStream(path.resolve('./' + name + '.jpg'))
        )
    });
};

module.exports = getpic;
本地运行成功后可将node_modules文件夹和已下载的图片删除
npm adduser
npm publish
修改后，记得修改版本号再重新上传
package.json:    "version": "1.0.1",   `名字不能和网上的重复`
npm publish



#################    20170725  global  #####################
异步函数
回调函数

项目工作流程



###################  做自己的小程序   ##############
在package.json里添加：  
"bin":{
    "download-pic-l":"index.js"
},

下载:
npm install request --save
npm install cheerio --save

下载并安装：npm install -g download-pic-l
运行：download-pic-l -t www.qq.com

去重: SET

###################     003 Os&Path&QueryString&Url&Child Propcess   ############E#############

设置中打开language --> Node.js and NPM --> enable打开




#################   npm install mysql --save   ##################

安装 express
#################   npm install express --save   ##################

npm run build

获取数据库：
1. 截取前端的代码（react生成的build中的static），放入static中。
2.  修改以前的路径  2.修改 /20170713/react/index.php/   改为  /




nodejs  v4.4.4    git

修改json,把要用到的下载的插件及编号，添加进去

nodejsnews

package.json的内容：
dependencies


把  '/'   放在最后

【1】准备：
1.把自己的index.js-->重命名为-->server.js。
2.package.json中修改为start:node server.js
3.所有js的第一行添加 'use strict'。 【因为用到了ES6】
4.index.html 页面中，不需要/public，直接/static就行。


【2】上传：
1.git clone 
2.cd 进去
3.把他的server.js用自己的替换掉（保留原有的 port = 10808 端口）
4.把自己的dependencies的东西放进他的里面。
5.把数据库所有的东西（名字、链接、）要换掉
6.上传




#################   webpack   ##################
###网址：         webpack.js.org
在webpack.js上、github上、npmjs上搜


npm install -g    
//-g  是安装到全局

documentation 配置
guides          向导

1.【配置】:
npm install -g webpack   
npm install -g webpack-dev-server
npm install webpack --save
npm install webpack-dev-server --save

###   示例
  
src/a.js:
`var str = 'hello';
 export default str;`
src/b.js:
`import cc from './a.js';
 alert(cc);
`
cmd中执行: `webpack src/b.js js/dist.js`
html中引入 `<script src="js/dist.js"></script>`

再写 
`webpack-config.js`
 执行`webpack -w`
 
 loader --> module
 
 【配置】:
npm install node-sass --save
npm install style-loader --save
npm install css-loader --save
npm install sass-loader --save
npm install file-loader --save
npm install url-loader --save
npm install html-webpack-plugin --save
npm install clean-webpack-plugin --save



webpack.config.js升级后
运行 · webpack -w · 执行【监测src中的变化来编译】



############     利用webpack将antd中需要的组件抽出来    ###########

inline-source

执行：
webpack-dev-server --open

npm start


###  需要在设置中关掉  safe write

【配置】:
npm install react --save
npm install react-dom --save
npm install babel-loader --save
npm install babel-core --save
npm install babel-preset-es2015 --save
npm install babel-preset-react --save
npm install antd --save


tree
react官网复制代码

nate-river的配置信息
new webpack.DefinePlugin({
            'process.env': {
                'NODE_ENV': JSON.stringify('production')
            }
        }),
        new webpack.optimize.UglifyJsPlugin({
            compress: {
                warnings: false
            }
        }),

```

