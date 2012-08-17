## uzai-html编码规范v0.1

1. 页面顶部必须添加文档类型;统一使用&lt;!DOCTYPE html&gt;,它更简洁，向后兼容，并且现代浏览器都认识它。

2. 每个页面必须有title标签，由于搜索引擎对title长度的限制，长度控制在30个汉字以内。

3. 引用外部css文件时,&lt;link&gt;标签必须关闭。

4. head区代码顺序：“编码” “标题” “&lt;meta&gt;区域” “样式” “脚本”

5. 所有标签、属性必须小写，属性值必须用引号“”，不允许缩写。

6. 所有标签必须关闭。如现在存在：&lt;img width="12" height="12" border="0" style="padding: 0 5px;" src="http://r.uzaicdn.com/content/reg/image/wenhao.gif"&gt;

7. <img&gt;标签尽量要有alt属性。

8. 注释使用&lt;!-- 注释代码 --&gt;,注释中不要出现”-”，注释务必表达清楚意思，让团队其它人员能够看懂。大块区域务必添加注释。

9. 代码缩进统一为4个空格

10. 为了代码结构分离，不要在元素中写style或者绑定javascript事件。

11. 尽量将脚本代码放在&lt;/body&gt;标签前。

12. 提倡使用语义化的html5标签，如&lt;aside&gt; &lt;article&gt;等，会引入相关脚本让IE支持html5标签。

13. 不要使用table来进行布局。

14.  id不能重复出现，id仅使用在大的模块上，class可用在重复使用率高及子模块中，javascript预留钩子时，请以J_开头，如：J_txtName。
