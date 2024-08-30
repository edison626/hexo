---
title: 网络安全C10-2024.8.17
swiper_index: 10
top_group_index: 10
background: '#fff'
date: 2024-08-30 14:47:45
updated:
tags: 网络安全C10-2024.8.17
categories: 网络安全C10-2024.8.17
keywords:
description:
top:
top_img:
comments:
cover:
toc:
toc_number:
toc_style_simple:
copyright:
copyright_author:
copyright_author_href:
copyright_url:
copyright_info:
mathjax:
katex:
aplayer:
highlight_shrink:
aside:
ai:
---

# 网络安全C10-2024.8.17-二

## 1、使用html写一个网页，要求满足以下条件： 

（1）网页中含有任意一张图片，图片路径使用绝对路径，鼠标悬停在图片时出现“马哥教育”. 文本，且点击图片可跳转至马哥教育官方页面

（2）网页中包含账号、密码登录，且账号提前定义好是admin且不可更改，输入密码时显示加密形式 

 ```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>简单网页</title>
    <style>
        /* 样式定义 */
        .image-container img {
            width: 300px;
            height: auto;
        }

        /* 悬停时显示文本的样式 */
        .image-container:hover::after {
            content: "马哥教育";
        }

        /* 定义账号框不可更改 */
        #username {
            background-color: #f0f0f0;
            border: none;
            cursor: not-allowed;
        }
    </style>
</head>
<body>
    <h1>欢迎访问我的网页</h1>

    <!-- 图片部分 -->
    <div class="image-container">
        <a href="https://www.magedu.com" target="_blank">
            <img src="https://www.magedu.com/wp-content/uploads/2021/10/2021101103583647.jpg" alt="图片描述">
        </a>
    </div>

    <!-- 登录表单 -->
    <h2>登录</h2>
    <form>
        <label for="username">账号:</label>
        <input type="text" id="username" value="admin" readonly><br><br>

        <label for="password">密码:</label>
        <input type="password" id="password" placeholder="请输入密码"><br><br>

        <button type="submit">登录</button>
    </form>
</body>
</html>
 ```



## 2、判断题 

### （1）Java是编译型语言。             

**答案：正确。**

解释：Java是一种编译型语言，在执行之前需要将代码编译为字节码（bytecode），然后由Java虚拟机（JVM）解释和执行。                                   

### （2）Javascript中，不区分大小写字母，也就是说A和a是同一个变量。       

**答案：错误。**

解释：JavaScript是区分大小写的，因此A和a被视为不同的变量。

### （3）Javascript中的常量包括String、Number、Boolean、Null、Undefined。      

**答案：错误。**

解释：这些是JavaScript中的基本数据类型，而非常量。常量在JavaScript中是通过const关键字定义的。

### （4）String字符串的语法中既可以使用单引号，也可以使用双引号。            

**答案：正确。**

解释：在JavaScript中，字符串既可以用单引号' '包裹，也可以用双引号" "包裹。

### （5）typeof是用来判断变量类型，不可以当作运算符使用。            

**答案：错误。**

解释：typeof是一个运算符，用来判断变量的数据类型，因此它是可以当作运算符使用的。        

### （6）任何值和 undefined 运算，undefined 可看做0运算。                     

**答案：错误。**

解释：undefined并不会被当作0参与运算。与undefined进行的数学运算通常会导致NaN（Not a Number）的结果。

 

## 3、请分别描述下列代码中“+”的作用。 

（1）

```html
console.log("年龄：" + 20); 
```

**作用：字符串拼接。**

解释：这里的+操作符用于将字符串"年龄："与数字20拼接在一起。最终结果是字符串"年龄：20"，因此输出的结果是"年龄：20"。    

（2）

```html
console.log(11+22+33); 
```

**作用：数学加法运算。**

解释：这里的+操作符用于进行加法运算。首先计算11 + 22，结果是33，然后再加上33，最终输出结果是66。    

（3）

```html

```



console.log("网络+安全");        

**作用：字符串本身包含****+****符号。**

解释：在这个例子中，+符号是字符串的一部分，console.log直接输出整个字符串"网络+安全"，并没有执行任何运算。

（4）       

```html    
var a = 1; 
var b = 2; 
console.log("a" + b);  
```

**作用：字符串拼接。**

解释：这里的+操作符用于将字符串"a"与变量b的值（2）拼接在一起，最终输出结果为"a2"。此处，b的值被转换成字符串后与"a"拼接。            

（5）        

```html              
var a = 1; 
var b = 2; 
console.log("a + b");  
```

**作用：字符串本身包含****+****符号。**

解释：在这个例子中，"a + b"是一个完整的字符串，并没有执行任何运算。输出结果就是字符串"a + b"本身。 

## 4、计算下述代码的打印值 

 ```js
var a = 10; 
var b = 10; 
console.log(a++);  
console.log(++a);  
console.log(--b);  
console.log(b--); 

//打印结果
10
12
9
9
 ```



5、分别使用行内式、内嵌式、引入外部文件的方法造成网页弹窗，要求触发弹窗的JS命令不止一种。 

 **1. 行内式（Inline Script）**

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>行内式弹窗示例</title>
</head>
<body>
    <button onclick="alert('这是一个行内式弹窗');">点击我触发弹窗</button>
    <button onclick="confirm('确认消息框：确定吗？');">点击我触发确认框</button>
</body>
</html>
```

**2. 内嵌式（Embedded Script）**

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>内嵌式弹窗示例</title>
</head>
<body>
    <button id="alertButton">点击我触发弹窗</button>
    <button id="promptButton">点击我触发提示框</button>

    <script>
        document.getElementById('alertButton').onclick = function() {
            alert('这是一个内嵌式弹窗');
        };

        document.getElementById('promptButton').onclick = function() {
            prompt('提示框：请输入你的名字');
        };
    </script>
</body>
</html>
```

**3. 引入外部文件（External Script）**

**外部文件（script.js）：**

```js
function showAlert() {
    alert('这是一个外部文件弹窗');
}

function showConfirm() {
    confirm('确认消息框：你确定吗？');
}
```

**HTML 文件：**

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>引入外部文件弹窗示例</title>
</head>
<body>
    <button onclick="showAlert();">点击我触发弹窗</button>
    <button onclick="showConfirm();">点击我触发确认框</button>

    <script src="script.js"></script>
</body>
</html>
```

