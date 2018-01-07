<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->
<!-- code_chunk_output -->

* [区块元素](#区块元素)
	* [关于标题的写法](#关于标题的写法)
	* [区块引用](#区块引用)
	* [列表](#列表)
	* [代码区块](#代码区块)
	* [分割线](#分割线)
* [区段元素](#区段元素)
	* [链接](#链接)
	* [强调](#强调)
	* [代码](#代码)
	* [图片](#图片)
* [其他](#其他)
	* [数学公式](#数学公式)
	* [导入文件](#导入文件)

<!-- /code_chunk_output -->


学习Markdown语法 
==============

## 快捷键
ctr+shift+m 打开预览   
ctr+shift+p 打开vscode运行命令行

## 区块元素
### 关于标题的写法
标题写法有两种，一种是使用底线的形式利用=和-进行高阶和二级标题的书写；一种是在行首使用#的个数来表示标题的等级。如下所示为行首使用#的效果

    # 这是H1
    ## 这是H2
    ### 这是H3
    #### 这是H4
    ##### 这是H5
    ###### 这是H6


### 区块引用
-----------
markdown标记区块引用为行首使用>标记, 可以每行首使用>，也可段落前使用>标记，效果如下：
>This is a blockquote with two paragraphs.
这就是区块引用的效果，看着还挺不错的，使用真的很简单。
>>这是嵌套使用的效果
>
>### 区块内也可以使用Markdown的语法

### 列表
-----
Markdown支持有序列表和无序列表

无序列表可以使用*、+和-作为标记
* 项目1
* 项目2
* 项目3

+ 项目1
+ 项目2

- [ ] 项目1
- [x] 项目2

有序列表可以使用数字加引文句点：
1. 项目1
2. 项目2
3. 项目3

HTML方式
<ol>
<li>Bird</li>
<li>Mchale</li>
<li>Parish</li>
</ol>

前面的数据可以是一样：
1. 哈哈1
1. 哈哈2
1. 哈哈3

或者不连续的：
1. 嘿嘿1
8. 嘿嘿2
5. 嘿嘿3

*   Lorem ipsum dolor sit amet, consectetuer adipiscing elit. 
    Aliquam hendrerit mi posuere lectus. 
1998\. Vestibulum enim wisi, viverra nec,   
    ringilla in, laoreet vitae, risus.
*   Donec sit amet nisl. Aliquam semper ipsum sit amet velit. 
    Suspendisse id sem consectetuer libero luctus adipiscing.



### 代码区块
----------
简单的缩进4个空格或一个制表符就可以

    #include <iostream>
    int main(){
        std::cout<<"hello,world"<<std::endl;
        return 0;
    }

HTML可直接写：

    <div class="footer">
        &copy; 2004 Foo Corporation
    </div>


### 分割线
------
可以使用三个以上的*、-、_来建立一个分隔线，行内不能有其他东西，*、-和_中间可以有空格，如:
***
* **
---
___


## 区段元素
### 链接
Markdown支持两种形式的链接语法：行内式和参考式两种形式。

This is [a example](https://www.baidu.com/ "百度") inline link.

相对路径[haha](test1.jpg)

参考式的链接，在链接的方括号后面在加上另一个方括号，在第二个方括号中填入用以辨识的的链接标记：
This is [an example][1] reference-style link.

链接标记可以用如下方式进行标识，有点像论文中的参考文献。

[1]: https://www.baidu.com

链接内容定义的形式为：

* 方括号（前面可以选择性地加上至多三个空格来缩进），里面输入链接文字
* 接着一个冒号
* 接着一个以上的空格或制表符
* 接着链接的网址
* 选择性地接着 title 内容，可以用单引号、双引号或是括弧包着

下面这三种链接的定义都是相同：

    [foo]: http://example.com/  "Optional Title Here"
    [foo]: http://example.com/  'Optional Title Here'
    [foo]: http://example.com/  (Optional Title Here)

隐式链接标记，可以使用链接文字作为链接标记，而无需在链接标记中写入链接标记，如下：
[Baidu][]

[Baidu]: https://www.baidu.com

    [Baidu][]
    [Baidu]: https://www.baidu.com


### 强调
使用*和_作为标记强调的字符，具体使用如下：  

    *Hello*
    _Hello_
    **Hello**
    \*Hello\*
    *Hello *
*Hello*  
_Hello_  
**Hello**  
\*Hello\*  
*Hello *


### 代码
如果标记行内小段代码，可以使用反引号\`来标记，如：  

    This is a line of code `#include <iostream>`
    please don't use any `<blink>` tags.
This is a line of code `#include <iostream>`   
please don't use any `<blink>` tags.


### 图片
Markdown使用一种和链接相似的方式语法来插入图片， 同样也使用两种方式的样式：行内式和参考式。  
行内式的图片语法如下：

    ![Alt text](/path/to/image.jpg)
    ![Alt text](/path/to/image.jpg "Title")
详细叙述如下：
* 一个惊叹号 !
* 接着一个方括号，里面放上图片的替代文字
* 接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上 选择性的 'title' 文字。

参考式语法如下(结合链接理解，基本一样的)：
    
    ![Alt text][id]
    [id]: url/to/image.jpg "Title"

markdown没法指定图片的长宽，如果需要的话使用普通的`<img>`标签

eg:

    ![test image](test.jpg)
    <img src="test.jpg" width=200 height=120 align=center />
![test image](test.jpg)
`<img src="test.jpg" width=200 height=120 align=left />`   

## 其他
### 数学公式
使用`$...\$`或者`\(...\)`数学公式将会在行内显示
使用`$$...$$`或者`\[...\]` 或者\```math 中的数学表达式将在块内显示

    $f(x) = ax + b$ 
    \(f(x) = ax + b\)
    $$\sum_{n=1}^{100} n$$


$f(x) = ax + b$   
\(f(x) = ax + b\)
$$\sum_{n=1}^{100} n$$

### 导入文件
使用`@import "文件名"`,支持在线文件导入。
    
    @import "test.jpg" {width="300px"}
    @import "http://g.hiphotos.baidu.com/image/pic/item/908fa0ec08fa513d08b6a0ab376d55fbb2fbd9a3.jpg"

@import "test.jpg" {width="300px"}   

@import "http://g.hiphotos.baidu.com/image/pic/item/908fa0ec08fa513d08b6a0ab376d55fbb2fbd9a3.jpg" {width="300px"}

