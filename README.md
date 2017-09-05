#HTML  vs  XML  vs XHTML
###HTML：

超文本标记语言，是语法较为松散的、不严格的web语言；

###XML：

  XML扩展性比HTML强，可以创建个性化的标记语言，XML的标记语言可以自定义，可以提供更多的数据操作，而不像HTML一样，只能局限于按一定的格式在终端显示出来。HTML的功能只有浏览器放入显示和打印，仅仅适合静态网页的要求。
  XML的语法比HTML严格，由于XML的扩展性强，它需要稳定的基础规则来支持扩展。它的严格规则为：
a 起始和结束的标签相匹配
b 嵌套标签不能相互嵌套
c 区分大小写，相对应XML的严格规则，HTML语言并没有规定标签的绝对位置，也不区分大小写，而这些全部由浏览器来完成识别和更正。
d. XML与HTML互补，XML可以获得应用之间的相应信息，提供终端的多项处理要求，也能被其他的解析器和工具所使用，在现阶段，XML可以转化成相应的HTML，来适应当前浏览器的需求。
###XHTML：
a. XHTML要求有严谨的结构，所有标签必须关闭。如果是单独不成对的标签，在标签最后加一个"/"来关闭它。
b. 所有标签的元素和属性的名字都必须使用小写，与HTML不一样，XHTML对大小写是敏感的。
c. 一层一层的嵌套必须是严格对称
d. 所有的属性必须用引号""括起来。
e. 把所有<和&特殊符号用编码表示。
任何小于号（<），不是标签的一部分，都必须被编码为<
任何大于号（>），不是标签的一部分，都必须被编码为>
任何与号（&），不是实体的一部分的，都必须被编码为&
注：以上字符之间无空格。
f. 给所有属性赋一个值，XHTML规定所有属性都必须有一个值，没有值的就重复本身。
g. 图片必须有说明文字，每个图片标签都必须有alt说明文字。
#HTML语义化

基本上都是围绕着几个主要的标签，像标题（H1~H6）、列表（li）、强调（strong em）等等。根据内容的结构化（内容语义化），选择合适的标签（代码语义化）便于开发者阅读和写出更优雅的代码的同时让浏览器的爬虫和机器很好地解析。

###为什么要将HTML语义化？

a. 为了在没有CSS的情况下，页面也能呈现出很好地内容结构、代码结构:为了裸奔时好看；
b. 用户体验：例如title、alt用于解释名词或解释图片信息、label标签的活用；
c. 有利于[SEO](http://baike.baidu.com/view/1047.htm)：和搜索引擎建立良好沟通，有助于爬虫抓取更多的有效信息：[爬虫](http://baike.baidu.com/view/998403.htm)依赖于标签来确定上下文和各个关键字的权重；
d. 方便其他设备解析（如屏幕阅读器、盲人阅读器、移动设备）以意义的方式来渲染网页；
e. 便于团队开发和维护，语义化更具可读性，是下一步吧网页的重要动向，遵循W3C标准的团队都遵循这个标准，可以减少差异化。

#内容与样式分离

a. 写HTML时先不管样式，重点放在HTML的结构和语义化上，让HTML能体现页面结构或者内容，之后再写样式。
b. 写JS时，尽量不要用JS直接操作样式，而是通过给元素添加删除class来控制样式变化。
c. HTML内不允许出现属性样式，尽量不要出现行内样式。

#常见的meta标签
```
<meta charset = "utf-8">
```
设置页面编码方式，页面保存编码方式要与浏览器解析编码方式一致，否则易乱码。
```
<meta http-eqiv="X-UA-computible"  content="IE=edge,chrome=1">
```
对于双核浏览器或者安装了插件的IE浏览器，使用IE最新版本或者chrome内核进行渲染。
```
<meta name="viewport" content= "width=device-width,initial-scale=1,maximum-scale=1">
```
使页面在移动端上展示合理的大小。
```
<meta name="keywords" content="蘑菇街">
<meta name="description" content="购物天堂">
```
优化搜索引擎

# 文档声明

a. Html5的文档声明信息：
 ```
<!DOCTYPE html>
```
声明必须位于 HTML5 文档中的第一行，也就是位于标签之前。它告诉浏览器网页所使用的 Html 规范是什么，用HTML5标准解析渲染当前页面。
b. 严格模式是浏览器根据规范去显示页面；混杂模式是以一种向后兼容的方式去显示。

#浏览器乱码

HTML页面保存编码方式要与浏览器解析编码方式一致，否则易乱码。
解决方法：如果浏览器中显示乱码，但是页面源文件不是乱码，可以通过修改浏览器的编码方式看到正确的中文，如果在源文件中设置了正确的"charset"，就不需要修改浏览器的编码方式了。

#浏览器及内核

主流浏览器所使用的内核分类
Trident内核：IE,MaxThon,TT,The World,360,搜狗浏览器等
Gecko内核：Netscape6及以上版本，FF,MozillaSuite/SeaMonkey等
Presto内核：Opera7及以上
Webkit内核：Safari,Chrome等
典型的双核浏览器包括：
搜狗2.0：Trident内核和WebKit内核
傲游3.0Beta：Trident和WebKit内核
QQ浏览器5：Trident内核和WebKit内核
使用双核浏览器时，可以自动/手动切换内核来浏览网页。

#常用标签及应用场景

a. 标题h  h1~h6   h1代表页面最大的标题；h2是二级标题；h6是最弱的标题
```
 <h1>我的文章<h1>
 <h6>我的文章<h6>
```
b. 段落p表示大段文字
 ```
<p>abcdefghijklmnopqrstuvwxyz</p>
```
c. a链接，链接到一个地址 
```
<a href="http://jirengu.com" target=“blank” title="蘑菇街">蘑菇街.com</a>
```
d. img展示一张图片
```
![](a.png)
```
e. div给页面划分区块
```
<div id="header"></div>
```
f. ul无序列表用来表示并列的内容
```
<ul><li><a href="#">首页</a></li></ul>
```
g. ol有序列表用于表示带步骤或者编号的并列内容
```
<ol><li>关上冰箱门</li></ol>
```
h. dl dt dd 用于展示一系列标题内容的场景
```
<dl><dt>商品名称</dt><dd>青花瓷</dd></dl>
```
i. button按钮 
```
<button>点我</button>
```
j. span em strong 语义加强
```
<span>xx</span>
<em>xx</em>
<strong>xx</strong>
```
k. iframe用于嵌入一个页面
```
<iframe src="http://baidu.com" name="mypage"></iframe>
```
l. table用于展示表格 
```
<table><tr><th>name</th></tr></table>
```
