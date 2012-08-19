## uzai-javascript规范v0.1

### 一、编码注意

1. 代码引入，外部文件&lt;script src=”example.js” type=”text/javascript”&gt;&lt;/script&gt;，内联脚本&lt;script type=”text/javascript”&gt;//code&lt;/script&gt;

2. 尽量将代码放在&lt;/body&gt;前。避免现在页面中很多脚本文件。

3. 尽量不要使用全局变量，请使用闭包或者命名空间。变量声明应放成函数开始的地方，且需要使用var 来声明变量。

4. 命名 类命名: 首字母大写, 驼峰式命名. 如 UzaiClass; 函数命名: 首字母小写驼峰式命名. 如uzaiFunction();命名语义化，尽可能利用英文单词或其缩写。

5. 避免使用eval()方法。使用eval会导致代码压缩时出现异常。

6. 不要省略分号，不要省略花括号。

7. 注释，多行注释使用 /* */，单行注释使用//，注释务必表达清楚意思，让团队其它人员能够看懂。

8. 前后端交互使用标准的json格式。(属性和值使用引号，值为num或者boolean可以省去引号等)

9. 不要在块内声明一个函数。如
```javascript
if (x) {
    function foo() {}
}
```
应该写成
```javascript
if (x) {
    var fn = function(){}
}
```
10. 避免使用try-catch-finally,避免使用with。

11. 设置setTimeout() 和 setInterval() 时传递函数名而不是字符串

12. 使用变量缓存值 如果需要对某个dom对像多次使用，应该先缓存该对像，如
var exampleDom=$(“#example”)。再对exampleDom行操作。

13. 为了代码结构分离，不要在dom元素中绑定事件。减少reflow,注重性能。

### 二、代码结构

1. 基础core:base.js ->  jquery.js及一些常用方法。

2. 组件widget:结构如图
![组件结构](/uzai/Front/blob/master/images/widget.jpg?raw=true)

3. 页面代码直接写在&lt;/body&gt;前，或者单独存放，形式如同组件，按页面来命名。