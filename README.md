# Diary_April

## Diary 【4.1】

### gihub使用

1. mkdir + 空格  + 文件夹名 ——创建文件夹
2. cd + 空格 + 文件夹名 + /（正斜杠）  ——进入文件夹
3. git clone https://github .......... .git  —— 克隆项目到本地
4. 
## Diary 【4.11】
### 在Github Pages搭建自己写的页面
准备工作：

1. 需要你自己写的网页文件
2. 注册Github
3. 下载安装git

教程开始：

1. 步骤一：登录到Github上，新建一个repo，命名为test，勾选 initialize this repository with a README，点击create repository
2. 步骤二：打开settings，有一个Github Pages 的设置，点击 source 中的本来的 None ，使其变成 master 分支，也就是作为部署github pages 的分支，然后点击 save
3. 步骤三：页面刷新之后，再看 github pages 设置框处，多了一行网址，就是你的 github pages 的网址了,点击这个链接,就可以发现已经创建成功
4. 步骤四 ：打开此电脑，选择一个盘，比如 f 盘，右键空白处点击 git bash here
5. 步骤五：输入如下命令，用来在 f 盘创建 test 文件放你的github上的test repository，克隆test repository到 test 文件中。(命令是mkdir + 空格 + 文件名 ，进入刚刚的文件夹  cd + 空格 + 文件名 + / ，接下来git clone https:// 克隆项目到本地)
6. 步骤六： 将自己的网页文件复制粘贴至 f 盘的 test 文件中
7. 首先输入  git status   列出当前目录所有还没有被git管理的文件和被git管理且被修改但还未提交(git commit)的文件，也就是所有改动文件，红色字体标出。然后输入 git add .  (有个点) 表示添加当前目录下的所有文件和子目录，然后 再输入一次 git status 如果看见文件都变绿了 ，那么就代表 它们已经准备好了被提交（git commit）。
8. 步骤九：输入如下命令，将你的文件上传至远程 master 分支 git commit -m "modify" 提交修改为modify  再git pull 拉取一次 看看是否已经是最新的了
9. 输入最后一行 git push，按回车，等一会，会有弹出框让你输入你的 github 账号和密码。
10. 打开浏览器输入给你的网址加上你上传的 html 文件名 test.html，然后重重的按下回车

附录一：常用git命令：

$ git clone  //本地如果无远程代码，先做这步，不然就忽略

$ cd //定位到你blog的目录下

$ git status //查看本地自己修改了多少文件

$ git add . //添加远程不存在的git文件

$ git commit  -m "what I want told to someone" //提交修改

$ git push  //更新到远程服务器上

$ git rm //移除文件

参考地址：http://www.cnblogs.com/lijiayi/p/githubpages.html

## Diary 【4.18】
###  JS数组方法汇总 array数组元素的添加和删除

1. pop：删除原数组最后一项，并返回删除元素的值；如果数组为空则返回undefined 

    var a = [1,2,3,4,5]; 
    var b = a.pop(); //a：[1,2,3,4]   b：5 //不用返回的话直接调用就可以了
2. shift：删除原数组第一项，并返回删除元素的值；如果数组为空则返回undefined 

    var a = [1,2,3,4,5]; 
    var b = a.shift(); //a：[2,3,4,5]   b：1 
3. unshift：将参数添加到原数组开头，并返回数组的长度 

    var a = [1,2,3,4,5]; 
    var b = a.unshift(-2,-1); //a：[-2,-1,1,2,3,4,5]   b：7 
注：在IE6.0下测试返回值总为undefined，FF2.0下测试返回值为7，所以这个方法的返回值不可靠，需要用返回值时可用splice代替本方法来使用。 

4. push：将参数添加到原数组末尾，并返回数组的长度 
    var a = [1,2,3,4,5]; 
    var b = a.push(6,7); //a：[1,2,3,4,5,6,7]   b：7 
5. concat：返回一个新数组，是将参数添加到原数组中构成的 
    var a = [1,2,3,4,5]; 
    var b = a.concat(6,7); //a：[1,2,3,4,5]   b：[1,2,3,4,5,6,7] 
6. splice(start,deleteCount,val1,val2,...)：从start位置开始删除deleteCount项，并从该位置起插入val1,val2,... 
    var a = [1,2,3,4,5]; 
    var b = a.splice(2,2,7,8,9); //a：[1,2,7,8,9,5]   b：[3,4] 
    var b = a.splice(0,1); //同shift 
    a.splice(0,0,-2,-1); var b = a.length; //同unshift 
    var b = a.splice(a.length-1,1); //同pop 
    a.splice(a.length,0,6,7); var b = a.length; //同push 
7. reverse：将数组反序 
    var a = [1,2,3,4,5]; 
    var b = a.reverse(); //a：[5,4,3,2,1]   b：[5,4,3,2,1] 
8. sort(orderfunction)：按指定的参数对数组进行排序 （从小到大）
    var a = [1,2,3,4,5]; 
    var b = a.sort(); //a：[1,2,3,4,5]   b：[1,2,3,4,5] 
9. slice(start,end)：返回从原数组中指定开始下标到结束下标之间的项组成的新数组 
    var a = [1,2,3,4,5]; 
    var b = a.slice(2,5); //a：[1,2,3,4,5]   b：[3,4,5] 
10. join(separator)：将数组的元素组起一个字符串，以separator为分隔符，省略的话则用默认用逗号为分隔符 
    var a = [1,2,3,4,5]; 
    var b = a.join("|"); //a：[1,2,3,4,5]   b："1|2|3|4|5"

再给个利用数组模拟javaStringBuffer处理字符串的方法：

    /**
    * 字符串处理函数
    */
    function StringBuffer(){
        var arr = new Array;
        this.append = function(str){
            arr[arr.length] = str; 
        };
        this.toString = function(){   
            return arr.join(""); //把append进来的数组ping成一个字符串
        };
    }

今天在应用中突然发现join是一种把数组转换成字符串的好方法，故封装成对象使用了：
    
    /**
    * 把数组转换成特定符号分割的字符串
    */
    function arrayToString(arr,separator){
    if(!separator) separator = "";    //separator为null则默认为空
        return arr.join(separator); 
    }
查找数组包含的字符串

    /**
    * 查找数组包含的字符串
    */
    function arrayFindString(arr,string){
        var str = arr.join(""); 
        return str.indexOf(string); 
    }

## Diary 【4.19】
###  js中typeof和instanceof用法区别

typeof和instanceof都可以用来判断变量，它们的用法有很大区别：

typeof会返回一个变量的基本类型，只有以下几种：number,boolean,string,object,undefined,function；

alert(typeof(1));//number

alert(typeof("abc"));//string

alert(typeof(true));//boolean

alert(typeof(m));//undefined

如果我们想要判断一个变量是否存在，可以使用typeof：(不能使用if(a) 若a未声明，则报错)

if(typeof a != 'undefined'){ //变量存在}

instanceof返回的是一个布尔值，如：

var a = {};

alert(a instanceof Object);  //true

var b = [];

alert(b instanceof Array);  //true

需要注意的是，instanceof只能用来判断对象和函数，不能用来判断字符串和数字等，如：

var b = '123';

alert(b instanceof String);  //false

alert(typeof b);  //string

var c = new String("123");

alert(c instanceof String);  //true

alert(typeof c);  //object

另外，用instanceof可以判断变量是否为数组

大家都知道js中可以使用typeof来判断变量的基本类型，如：

alert(typeof '111'); // "string" 

alert(typeof 22); // "number" 

alert(typeof a); // "undefined" 

alert(typeof undefined); // "undefined" 

alert(typeof []); // "object"

但是这个方法不适用于来判断数组，因为不管是数组还是对象，都会返回object，这就需要我们需求其他的方法。

有几种方法可以拿来判断：

1、constructor属性

这个属性在我们使用js系统或者自己创建的对象的时候，会默认的加上，例如：

var arr = [1,2,3];  //创建一个数组对象

arr.prototype.constructor = Array;  //这一句是系统默认加上的

所以我们就可以这样来判断：

var arr = [1,2,3,1]; 

alert(arr.constructor === Array);   // true

2、instanceof

instanceof是检测对象的原型链是否指向构造函数的prototype对象的，所以我们也可以用它来判断：

var arr = [1,2,3]; 

alert(arr instanceof Array);   // true

最后，为了给大家一个结果，现写出一个终极解决方案：

判断数组终极解决方案

var arr = [1,2,3]; 

function isArrayFn(obj){  //封装一个函数

if (typeof Array.isArray === "function") { 

return Array.isArray(obj); //浏览器支持则使用isArray()方法

}else{                     //否则使用toString方法

return Object.prototype.toString.call(obj) === "[object Array]"; 

} 

} 

alert(isArrayFn(arr));// true


参考网址:http://blog.csdn.net/u014421556/article/details/52083215

## Diary 【4.20】
###  js如何判断一个对象{}是否为空对象，没有任何属性

备注. model.rows 只是一个object

    if (typeof model.rows === "object" && !(model.rows instanceof Array)){  
        // 判断是否是一个object  typeof（对象和数组都是object）  用instanceof排除不是数组
        model.rows = [model.rows];   转为数组
    }  
    当 model.rows = {};  //空集合时会报错

遍历JS对象属性的方法

    if (typeof model.rows === "object" && !(model.rows instanceof Array)){  
        var hasProp = false;  
        for (var prop in model.rows){  
            hasProp = true;  
            break;  
        }  
        if (hasProp){  
            model.rows = [model.rows];  
        }else{  
            throw "model.rows is empty object";  
            return false;  
        }  
    }  

JavaScript判断object/json 是否为空，可以使用jQuery的isEmptyObject()方法。

    function isEmptyObject(e) {  
        var t;  
        for (t in e)  
            return !1;  
        return !0  
    }  
    console.log($.isEmptyObject({"re": 2}));    //false  
    console.log(isEmptyObject());           //true  
    console.log(isEmptyObject({}));         //true  
    console.log(isEmptyObject(null));       //true  
    console.log(isEmptyObject(23));         //true  
    console.log(isEmptyObject({"te": 2}));      //false  

结束语 ：jQuery的isEmptyObject()方法实现的代码即简单又简洁，但最关键的是我们要理解原理。

参考地址：http://blog.csdn.net/testcs_dn/article/details/40431835

## Diary 【4.21】
###  json对象和js对象的区别

两者本来就是同一个东西

key用""引起来，是可选的。比如key里有点号，那就必须引起来

json就是javascript的对象字面量。只是因为他的字符串格式特别适合传递数据，所以其他语言加入了对他的支持

对于JS的字面量来说，这段文本仅仅是代码的一部分，相当于指令，而JSON文本，其本身就表示了数据

二者相同的地方是，看起来都是数据，而且恰巧又都是文本；不同的地方在于，JS字面量的文本是被**脚本引擎**直接解析的，而JSON的文本，如果要转化为JS对象的话，是交给**eval函数**来处理的，那么，如何理解**JSON的文本**，就取决于这个函数，而不是脚本引擎，因为这2者的处理根本就不在一个层面上

另外，JS必须交给**JS脚本引擎处理**，而**JSON的字符串**，**任何程序都能处理**，至于引号的问题，取决于JSON解析器的容忍程度，如果你愿意，也可按照自己的意愿写一个解析器，能够容忍包括不写引号，或者单/双引号，甚至其他任何符号作为边界符

参考网址：http://www.iteye.com/problems/102527
