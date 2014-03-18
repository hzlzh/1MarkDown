# MarkDown 团队统一书写规范 v1.0

由于 MarkDown 语法在细节的书写方式很多，为了让不同个体的文档传产出结构一致，提炼出此规范。
该规范遵循 [MarkDown 官方语法] 以及 [GitHub MakDown 语法]，旨在统一书写格式和代码风格，将多种写法统一。

*注：本文档符合自身规范，可视作demo，参看源码*

大家可以 `fork` 后形成自己团队的规范版本

## 1.1全局规范
<a name="top"></a>

* MarkDown 文件均使用`.md`作为后缀 (**小写字母**)
* 普通文本换行，使用行末尾`2空格`触发

## 格式规范

### 标题结构格式

1. 标题与紧贴的`上下正文`使用`1整行换行`隔开
2. `#`号和文字之间`1个空格`连接]
3. 标题层级如下，最多6级

```
# 顶级标题 等价于 title 和 <h1>
## 次级标题 等价于 <h2>
### 3级标题 等价于 <h3>
#### 4级标题 等价于 <h4>
##### 5级标题 等价于 <h5>
###### 6级标题 等价于 <h6>
####### 注：此行错误，标题层级最多6级 没有<h7>标签
```

### 加强和强调规范

以下两种写法都是正确的，请统一为**第一种**，即一律使用 `**加强` `*强调`

```
*emphasize*   **strong** 相当于<strong>标签和<em>标签
_emphasize_   __strong__
```

### 代码块规范

* 行内代码使用`1对波浪号` 如： \`hello world!\`
* 块级代码使用`3个波浪号` 或 `整体4空格缩进`，且上下均用`整合隔开`，如下:  (**占用7行**)

```  
<?php   
   echo '看我源码 - 3个波浪号';  
?>  
```

    <?php   
        echo '看我源码 - 4空格缩进';  
    ?>  
 
### 列表写法

* 列号`1.` 或者`* `后其后内容`空格`隔开
* 列表块前后`整行隔开` 如下：

```    
1. Windows  
2. Mac
3. iOS
    * iPhone
    * iPad
4. Android
```

**实际预览：**

1. Windows  
2. Mac
3. iOS
    * iPhone
    * iPad
4. Android

```    
* Windows  
*  Mac
*  iOS
*  Android
    1. v3.2
    2. v4.1
```

**实际预览：**

* Windows  
*  Mac
*  iOS
*  Android
    1. v3.2
    2. v4.1

### 其他标签规范

链接和Email
Inline:

```
An [example](http://url.com/ "Title")
```

引用样式标签 (titles are optional):

    An [example][id]. Then, anywhere
    else in the doc, define the link:

    [id]: http://example.com/  "Title"

Email:

```
An email <example@example.com> link.
```

插图
Inline (titles are optional):

```
![alt text](/path/img.jpg "Title")
```

引用式插图:

    ![alt text][id]
    
    [id]: /url/to/img.jpg "Title"


引用块及嵌套

> Email-style angle brackets
> are used for blockquotes.

> > And, they can be nested.

> #### Headers in blockquotes
> 
> * You can quote a list.
> * Etc.

内联代码

`<code>` 段落中的用法

也可以 `` `代码中包含波浪号` ``.
Block Code
Indent every line of a code block by at least 4 spaces or 1 tab.

我是普通文本块

    我是一个预格式化的
    代码块.

水平分割线
三个`连字符`:

---

### 表格规范

一个简单的表格看起来如下：

第一个头部 | 第二个头部 | 第三个头部
--------|---------|-------
内容格子 | 内容格子 | 内容格子
内容格子 | 内容格子 | 内容格子

每列的对齐可以通过在分割线上添加冒号来实现：

第一个头部 | 第二个头部 | 第三个头部
:--------|:---------:|-------:
左对齐 | 居中 | 右对齐
左对齐 | 居中 | 右对齐

### 页内锚标记

* [点我跳转到顶部](#11全局规范)   // 利用 `#`,`##` 生成 `id` 锚标签  
* [另一种锚标记](#top) // 利用 `<a name="top"></a>`

---

附：参考 Hello-World.md 源码，*注意换行的使用*

```
# Hello-World

这是一个范例文件格式
我是普通换行

## 我是<h2>标题

我是`<h2>`的内容

## 我是<h3>标题

* Windows  
*  Mac
*  iOS
*  Android

```

注：引用范例请参看源码底部

#### License

Released under [MIT](http://rem.mit-license.org/) LICENSE

[MarkDown 官方语法]: http://daringfireball.net/projects/markdown/
[GitHub MakDown 语法]: https://github.com/mojombo/github-flavored-markdown/issues/1