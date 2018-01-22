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
     
    



