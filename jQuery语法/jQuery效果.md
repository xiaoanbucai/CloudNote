### jQuery 效果

##### 显隐效果

###### hide() 和 show() 

方法来隐藏和显示 HTML 元素。

```
$(selector).hide(speed,callback);

$(selector).show(speed,callback);
```

**可选的** speed 参数规定隐藏/显示的速度，可以取以下值："slow"、"fast" 或毫秒。

**可选的** callback 参数是隐藏或显示完成后所执行的函数名称。

###### toggle() 方法

来切换 hide() 和 show() 方法。

```
$(selector).toggle(speed,callback);
```

#####  淡入淡出效果

###### fadeIn() 方法

用于淡入已隐藏的元素。

```
$(selector).fadeIn(speed,callback);
```

**可选的** speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。.

**可选的** callback 参数是 fading 完成后所执行的函数名称。

######  fadeOut() 方法

用于淡出可见元素。

```
$(selector).fadeOut(speed,callback);
```

######  fadeToggle() 方法

可以在 fadeIn() 与 fadeOut() 方法之间进行切换。

```
$(selector).fadeToggle(speed,callback);
```

######  fadeTo() 方法

允许渐变为给定的不透明度（值介于 0 与 1 之间）。

```
$(selector).fadeTo(speed,opacity,callback);
```

##### 滑动效果

###### slideDown() 方法

用于向下滑动元素。

```
$(selector).slideDown(speed,callback);
```

**可选的** speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。

**可选的** callback 参数是滑动完成后所执行的函数名称。

###### slideUp() 方法

用于向上滑动元素。

```
$(selector).slideUp(speed,callback);
```

######  slideToggle() 方法

可以在 slideDown() 与 slideUp() 方法之间进行切换。

```
$(selector).slideToggle(speed,callback);
```

##### 动画

###### animate() 方法

用于创建自定义动画。

```
$(selector).animate({params},speed,callback);
```

**必需的** params 参数定义形成动画的 CSS 属性。

**可选的** speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。

**可选的** callback 参数是动画完成后所执行的函数名称。

**可以用 animate() 方法来操作所有 CSS 属性吗？**

是的，几乎可以！不过，需要记住一件重要的事情：当使用 animate() 时，必须使用 Camel 标记法书写所有的属性名，比如，必须使用 paddingLeft 而不是 padding-left，使用 marginRight 而不是 margin-right，等等。同时，色彩动画并不包含在核心 jQuery 库中。

##### 停止动画

###### stop() 方法

用于停止动画或效果，在它们完成之前。

stop() 方法适用于所有 jQuery 效果函数，包括滑动、淡入淡出和自定义动画。

```
$(selector).stop(stopAll,goToEnd);
```

**可选的** stopAll 参数规定是否应该清除动画队列。默认是 false，即仅停止活动的动画，允许任何排入队列的动画向后执行。

**可选的** goToEnd 参数规定是否立即完成当前动画。默认是 false。因此，默认地，stop() 会清除在被选元素上指定的当前动画。

##### Callback 方法

###### Callback 函数

在当前动画 100% 完成之后执行。

实例：

```
$("button").click(function(){
  $("p").hide("slow",function(){
    alert("段落现在被隐藏了");
  });
});
```

##### 链(Chaining)

Chaining 允许我们在一条语句中运行多个 jQuery 方法（在相同的元素上）。

链接（chaining）的技术，允许我们在相同的元素上运行多条 jQuery 命令，一条接着另一条。这样的话，浏览器就不必多次查找相同的元素。

例子：

```
$("#p1").css("color","red").slideUp(2000).slideDown(2000);
```

### 