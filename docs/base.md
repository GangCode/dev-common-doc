**一、HTML**
=============

1.HTML5 doctype
----------------

`   <!DOCTYPE html>`
2.ie 兼容模式
--------------
`   <meta http-equiv="X-UA-Compatible" content="IE=Edge">`
3.字符编码
-----------
`   <meta charset="UTF-8">`
4.引入 CSS 和 JavaScript 文件及其位置
-------------------------------------
`   <link rel="stylesheet" href="code-guide.css">`
`   <script src="code-guide.js"></script>`

-  样式文件要放置到脚本文件前；
-  尽量不要将脚本文件放到head标签之中，而是放到body闭合标签之前。

5.Html布尔属性不要赋值
----------------------
`   <input type="text" disabled>`
6.html标签
-----------

-  标签语义化，使用时要符合使用场景；
-  标签名统一小写；
-  子级标签与最近的附近标签之间保留2个空格【可在IDE中设置】；
-  不要使用内联样式；
-  不要使用内联脚本，若使用尽量不要使用多个`<script>`标签；
-  属性值要用双引号；

**二、CSS**
===========

1.为选择器分组时，将单独的选择器单独放在一行。
---------------------------------------------
<pre style="color:#EA5A46;background-color:#E2E4E6;font-size:14px;">
<code>
    .selector,
    .selector-secondary,
    .selector[type="text"] {
        padding: 15px;
        margin-bottom: 15px;
    }
</code>
</pre>
2.每条声明语句后应该插入一个空格，每条声明语句结尾加分号。
-------------------------------------------------------
<pre style="color:#EA5A46;background-color:#E2E4E6;font-size:14px;">
<code>
    .test{
        padding:  15px;
    }
</code>
</pre>
3.颜色的十六进制值小写和简写
----------------------------
    如白色：#fff
4.选择器中的属性添加双引号
--------------------------
    input[type="text"]
5.class多用于公用样式，多用样式组合，少用样式继承。
-------------------------------------------------

6.使用CSS3的的某些特性时加浏览器前缀。【可用css与编译器处理】
------------------------------------------------------------

7.注释
-------
    使用正确的注释 `/* desc */`

**三、Javascript**
=======================

1.少用全局变量
---------------

2.脚本模块化
-------------

3.功能模块以函数为单位，多使用纯函数
------------------------------------

4.动态生成的html使用模版编译
----------------------------

5.函数的参数使用对象来传参
---------------------------
`   function test(param){`
`       var res = param.a + param.b + param.c;`
`       return res;`
`   }`
`   test({`
`       a:1,`
`       b:2,`
`       c:3`
`   });`
6.采用缓存
-----------

    如查找DOM时，可将父级元素的DOM缓存，
`  var $tr = $('tr');`
`  var tds = $tr.children('td');`
7.字符串使用单引号。
--------------------

8.条件分支
----------

-  使用条件判断时将不符合条件的分支放到最前面，并加入分支结束语句；
-  分支超过3个后使用 switch分支；

9.使用注释
-----------

-  函数加文档注释
`  /**`
`    * 功能描述`
`    * @参数名称 {参数类型} 参数说明 `
`  */`
-  去除不必要的注释；

**四、命名规范**
====================

1.命名尽量简写
---------------

    *文件命名:文件名小写*

-  css文件：css-module.css
-  js文件：js.modules.js
-  html文件：html_modulle.html

2.样式选择器命名
-----------------

-  class：.msg-list   【多个单词使用中划线】
-  id: #td_no     【多个单词使用下划线】
-  name : msg_query  【多个单词使用下划线】

3.脚本中变量函数的命名
----------------------
使用驼峰命名法，var priceSum = 0;
