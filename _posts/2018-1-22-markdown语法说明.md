# Markdown语法说明  

### 段落和换行  
换行：两个空格加上换行。

### 标题
一个「#」号表示一级标题 即h1  
两个「#」号表示二级标题 即h2  
...  
六个「#」号表示六级标题 即h3  

### 区块引用 Blockquotes
区块引用: 在每行的最前面加上> 如下  

> xxx  
> >xxx

### 列表  
Markdown 支持有序列表和无序列表。  
无序列表使用星号、加号或是减号作为列表标记：  
<div>
  
*   Red
*   Green
*   Blue
  
+   Red
+   Green
+   Blue

-   Red
-   Green
-   Blue

</div>
-   Red
-   Green
-   Blue
有序列表则使用数字接着一个英文句点：
<div>
1.  Bird
2.  McHale
3.  Parish
</div>  

1. xxx
2. xxx
3. ccc 

当然，项目列表很可能会不小心产生，像是下面这样的写法：
   <div> 1986. What a great season.
   </div>
   换句话说，也就是在行首出现数字-句点-空白，要避免这样的状况，你可以在句点前面加上反斜杠。  
   
   <code>1986\. What a great season.</code>

### 代码区块
要在 Markdown 中建立代码区块很简单，只要简单地缩进 4 个空格或是 1 个制表符就可以  

    xxxx4 个空格或是 1 个制表符  
    
在代码区块里面， & 、 < 和 > 会自动转成 HTML 实体，这样的方式让你非常容易使用 Markdown 插入范例用的 HTML 原始码，只需要复制贴上，再加上缩进就可以了，剩下的 Markdown 都会帮你处理，例如:  
 
     <div class="footer">
     &copy; 2004 Foo Corporation
     </div>  
    
会被转换为：  

    <pre><code>&lt;div class="footer"&gt;
    &amp;copy; 2004 Foo Corporation
    &lt;/div&gt;
    </code></pre>
     
### 分隔线   
你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：  

    * * *

    ***

    *****

    - - -

    ---------------------------------------



***

### 链接
Markdown 支持两种形式的链接语法： 行内式和参考式两种形式。  

不管是哪一种，链接文字都是用 [方括号] 来标记。  

要建立一个行内式的链接，只要在方块括号后面紧接着圆括号并插入网址链接即可，如果你还想要加上链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可，例如：  

    This is [an example](http://example.com/ "Title") inline link.

    [This link](http://example.net/) has no title attribute.  
    
会产生：  

    <p>This is <a href="http://example.com/" title="Title">
    an example</a> inline link.</p>

    <p><a href="http://example.net/">This link</a> has no
    title attribute.</p>
如果你是要链接到同样主机的资源，你可以使用相对路径：

    See my [About](/about/) page for details.

参考式的链接是在链接文字的括号后面再接上另一个方括号，而在第二个方括号里面要填入用以辨识链接的标记：
    
    This is [an example][id] reference-style link.
你也可以选择性地在两个方括号中间加上一个空格：  
    
    This is [an example] [id] reference-style link.
    
接着，在文件的任意处，你可以把这个标记的链接内容定义出来：

    [id]: http://example.com/  "Optional Title Here"  
    
This is [an example](http://example.com/ "Title") inline link.  

This is [an example] [id] reference-style link.  

[id]: http://example.com/  "Optional Title Here"  


### 强调
Markdown 使用星号（*）和底线（_）作为标记强调字词的符号，被 * 或 _ 包围的字词会被转成用 <em> 标签包围，用两个 * 或 _ 包起来的话，则会被转成 <strong>，例如：
    
    *single asterisks*

    _single underscores_

    **double asterisks**

    __double underscores__

会转成：
    
    <em>single asterisks</em>

    <em>single underscores</em>

    <strong>double asterisks</strong>

    <strong>double underscores</strong>
    

你可以随便用你喜欢的样式，唯一的限制是，你用什么符号开启标签，就要用什么符号结束。

强调也可以直接插在文字中间： un*frigging*believable

  *single asterisks*

  _single underscores_

 **double asterisks**

 __double underscores__
 
 但是如果你的 * 和 _ 两边都有空白的话，它们就只会被当成普通的符号。
 如果要在文字前后直接插入普通的星号或底线，你可以用反斜线：
 
     \*this text is surrounded by literal asterisks\*
     
