jQuery 语法是通过选取 HTML 元素，并对选取的元素执行某些操作。

###  jQuery语法

####  jQuery基础语法

$(selector).action()

- 美元符号定义 jQuery
- 选择符（selector）"查询"和"查找" HTML 元素
- jQuery 的 action() 执行对元素的操作

jQuery 库是一个 JavaScript 文件，您可以使用 HTML 的 <script> 标签引用它：

```
<head> 
    <script src="jquery.min.js"></script> 
</head>
```

或者使用在线的CDN：

```
<head> 
    <script src="https://ajax.aspnetcdn.com/ajax/jquery/jquery-1.9.0.min.js"></script> 
</head>
```

#### jQuery 入口函数

```
$(document).ready(function(){
    // 执行代码
});
或者
$(function(){
    // 执行代码
});
```

#### JavaScript 入口函数

```
window.onload = function () {
    // 执行代码
}
```

#### jQuery 入口函数与 JavaScript 入口函数的区别

- jQuery 的入口函数是在 html 所有标签(DOM)都加载之后，就会去执行。

- JavaScript 的 window.onload 事件是等到所有内容，包括外部图片之类的文件加载完后，才会执行。

  ![](image/load和ready区别.jpg)
