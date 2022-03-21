---
layout: post
title: HTML入门
date: 2022-03-21
author: syy
tags: [HTML,笨比sy]
comments: false
toc: true
pinned: false
---

# HTML入门

### 语法和结构

#### 属性

![image-20220303113305854](C:\Users\sy\AppData\Roaming\Typora\typora-user-images\image-20220303113305854.png)

#### 大小写

本学期建议大家在编写网页时注意以下准则，避免出现语法错误：

‒ **标签名和属性名称小写** 

‒ 所有属性都放在开始标签的尖括号内。

‒ 标签名称和属性之间以及不同属性之间都用空格分隔 

‒ 属性值放在属性之后，用等号分隔

‒ 属性值应该被包含在英文双引号中

#### 基本结构

![image-20220303113750165](C:\Users\sy\AppData\Roaming\Typora\typora-user-images\image-20220303113750165.png)

##### meta

-定义HTML文档的编码格式，在HTML5之后变得简洁

​	meta charset

-用于提供与浏览器或者搜索引擎的相关信息

​	meta name

###### #召唤术

​	meta:vp	[tab]

##### link

-用于引入其他的文件，如CSS文件和显示在浏览器标题/收藏夹的图标

#### 语法

##### p

###### em

###### <em>文字</em>

###### strong

<strong>文字</strong>

###### span

对元素进行区隔使其以不同样式显示（不具有任何样式，需要结合CSS

<span>段落文字</span>

###### br

段内换行，使后面的内容显示于下一行，无空行（仍属于同一段落）

文字<br>文字

###### sup/sub

上标superscript，下标subscript

<sup>文字</sup><sub>文字</sub>

###### blockquote

块引用，默认为左右两侧缩进

<blockquote>引用的文字</blockquote>

###### pre

代码块，保留空格和换行符

<pre>文字   文字</pre>

###### #召唤术

lorem字数 [enter]

##### list

###### ul

无序列表unordered list 

<ul>
    <li>list 1</li>
    <li>list 2</li>
</ul>
###### ol

有序列表ordered list

<ol>
    <li>list 1</li>
    <li>list 2</li>
</ol>

type可以是A/a/I/i/1

###### dl

定义列表definition list

<dl>
	<dt>definition term</dt>
    <dd>definition description</dd>
</dl>

##### 表格

<table>
    <caption>title</caption>
    <tr>
        <th>table header1</th>
        <th>table header2</th>
    </tr>
    <tr>
        <td>table data1</td>
        <td>table data2</td>
    </tr>
</table>

tr=table row

thead=表格头部信息

tbody=表格主体信息

tfoot=表格页脚信息

colspan=跨列合并

rowspan=跨行合并

##### 特殊字符和注释

<!--实体名称对大小写敏感-->

![image-20220304105102756](C:\Users\sy\AppData\Roaming\Typora\typora-user-images\image-20220304105102756.png)

注释大全：https://www.w3school.com.cn/tags/index.asp

#### 元素

##### div(sion)

| logo     | logo        |
| -------- | ----------- |
| 页面头部 | header      |
| 导航     | nav         |
| 广告     | banner      |
| 内容     | container   |
| 主体内容 | maincontent |
| 侧栏内容 | side        |
| 搜索框   | search      |
| 页面底部 | footer      |

##### HTML5

| 头部：logo&导航          | header  |
| ------------------------ | ------- |
| 导航                     | nav     |
| 独立区块                 | article |
| 划分：内含标题元素       | section |
| 附属信息                 | aside   |
| 页脚：版权信息、联系信息 | footer  |

### CSS

#### 语法

##### 定义格式

<style>
    selector{//样式名称	
        property:value;//样式属性&属性值
}
</style>

##### 单位

###### 绝对单位

1 in = 2.54cm	1 pt = 1/72 in	1 pc = 12 pt 

cm\mm

###### 相对单位

| 单位 | 说明                                                  |
| ---- | ----------------------------------------------------- |
| px   | 像素，相对于显示器的屏幕分辨率                        |
| em   | 相对于当前元素的字体大小                              |
| rem  | 相对于默认基础字体的大小，即相对于 html元素的字体大小 |
| %    | 相对于父级元素的百分比                                |

#### 盒模型

<img src="C:\Users\sy\AppData\Roaming\Typora\typora-user-images\image-20220313110058734.png" alt="image-20220313110058734" style="zoom:50%;" />

##### margin

| 分开写              | 简写                                 |
| ------------------- | ------------------------------------ |
| margin-top: 0;      | margin: 10px//四个方向               |
| margin-right: auto; | margin: 0 auto;//上下 左右           |
| margin-bottom: 0;   | margin: 0 auto 10px;//上 左右 下     |
| margin-left: auto;  | margin: 10px 20px 30px 40px;//顺时针 |

##### padding

| 分开写 | 简写                                |
| ------ | ----------------------------------- |
| 同上   |                                     |
|        | padding: 10px 20px;//上下 左右      |
|        | padding:10px 20px 20px;//上 左右 下 |
|        | 同上                                |

##### border

<img src="C:\Users\sy\AppData\Roaming\Typora\typora-user-images\image-20220313111611725.png" alt="image-20220313111611725" style="zoom:50%;" />

e.g.	border-top: 1px solid #000;

##### CSS重置

#### 颜色

##### 16进制

#rrggbb

<img src="C:\Users\sy\AppData\Roaming\Typora\typora-user-images\image-20220314182637755.png" alt="image-20220314182637755" style="zoom:50%;" />

##### RGBA形式

rgba(0,0,0,0)~(255,255,255,1.0)	rgb(0%,100%,0%)

##### CSS颜色规范

147种

##### HSLA形式

色相饱和度用hsl(h,s,l)函数来指定颜色 

− h用来指定色相，其取值范围是0-360 

− s用来指定饱和度，其取值范围是0%-100% 

− l用来表示明度，其取值范围是0%-100%

− a表示透明度，其取值范围为：0.0-1.0

##### background-color 前景色

*建立设计规范*

#### 选择器

<img src="C:\Users\sy\AppData\Roaming\Typora\typora-user-images\image-20220314184055126.png" alt="image-20220314184055126" style="zoom:50%;" />

##### 类型选择器

header	h1	blockquote	p	footer

```
p{
​	color:#333;
}
```

##### 类选择器

`. question{color:#A40000}`

#<p class="question">类样式的使用</p>

##### ID选择器

`#meta_content`

```
#container{

​	width:677px;

​	margin:0 auto;

}
```

##### 后代选择器

<!--儿子 孙子 重孙子...-->

`wenda p{text-indent: 0}`

选择selectorA的所有下级selectorB元素

​	`selectorA selectorB`

##### 子元素选择器

<!--儿子-->

`selectorA>selectorB`

选择selectorA的直接后代selectorB元素

##### 通配符选择器

```
*{

​	margin:0;

​	padding:0

}
```

#### 常用的文本样式

| 文字颜色     | color            |                       |
| :----------- | ---------------- | --------------------- |
| 背景颜色     | background-color | 不可继承              |
| 字体         | font-family      | 设置多个字体;可以继承 |
| 字号         | font-size        | px                    |
| 加粗方式     | font-weight      | 见下                  |
| 斜体         | font-style       | normal;italic;oblique |
| 字间距       | letter-spacing   |                       |
| 行高         | line-height      |                       |
| 首行缩进     | text-indent      |                       |
| 水平对齐方式 | text-align       | center                |

<img src="C:\Users\sy\AppData\Roaming\Typora\typora-user-images\image-20220317111924177.png" alt="image-20220317111924177" style="zoom:50%;" />

<img src="C:\Users\sy\AppData\Roaming\Typora\typora-user-images\image-20220317111942493.png" alt="image-20220317111942493" style="zoom:50%;" />
