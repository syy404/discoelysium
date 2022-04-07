---
layout: post
title: 🐒HTML入门(更新到超链接)
date: 2022-03-29
author: 笨比sy
tags: [HTML,Newbie]
comments: false
toc: true
pinned: false
---

救世啊（悲）⚠本文为防止markdown自动吃掉HTML代码，在部分元素声明前多加了一道斜杠，参考时请去除食用（

<!--more-->


<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203231152182.png" alt="image-20220323115253921" style="zoom:25%;" />

## 语法和结构

#### 属性

![image-20220303113305854](https://cdn.jsdelivr.net/gh/syy404/photospace/202203230954244.png)

#### 大小写

本学期建议大家在编写网页时注意以下准则，避免出现语法错误：

‒ **标签名和属性名称小写** 

‒ 所有属性都放在开始标签的尖括号内。

‒ 标签名称和属性之间以及不同属性之间都用空格分隔 

‒ 属性值放在属性之后，用等号分隔

‒ 属性值应该被包含在英文双引号中

#### 基本结构

![image-20220303113750165](https://cdn.jsdelivr.net/gh/syy404/photospace/202203230954532.png)

**meta**

-定义HTML文档的编码格式，在HTML5之后变得简洁

​	meta charset

-用于提供与浏览器或者搜索引擎的相关信息

​	meta name

###### #召唤术

​	meta:vp	[tab]

**link**

-用于引入其他的文件，如CSS文件和显示在浏览器标题/收藏夹的图标

#### 语法

##### 文字   

- **p**

- em

​		</em>文字</em>

- strong

​		</strong>文字</strong>

- span

​		对元素进行区隔使其以不同样式显示（不具有任何样式，需要结合CSS

​		</span>段落文字</span>

- br

​		段内换行，使后面的内容显示于下一行，无空行（仍属于同一段落）

​		文字</br>文字

- sup/sub

​		上标superscript，下标subscript

​		</sup>文字</sup>//上标

​		</sub>文字</sub>

- blockquote

块引用，默认为左右两侧缩进

</blockquote>引用的文字</blockquote>

- pre

代码块，保留空格和换行符

</pre>文字   文字</pre>

###### #召唤术

​	lorem字数 [enter]

**list**

- ul

​		无序列表unordered list 

​		</ul>
​    		<li>list 1</li>
​    		<li>list 2</li>
​		</ul>


- ol

​		有序列表ordered list

​		</ol>
​			<li>list 1</li>
​			<li>list 2</li>
​		</ol>


​		type可以是A/a/I/i/1

- dl

​		定义列表definition list

​		</dl>
​			<dt>definition term</dt>
​    		<dd>definition description</dd>
​		</dl>

**表格**

​		</table>
​    		<caption>title</caption>
​    		<tr>
​        		<th>table header1</th>
​        		<th>table header2</th>
​    		</tr>
​    		<tr>
​        		<td>table data1</td>
​        		<td>table data2</td>
​    		</tr>
​		</table>


​		tr=table row

​		thead=表格头部信息

​		tbody=表格主体信息

​		tfoot=表格页脚信息

​		colspan=跨列合并

​		rowspan=跨行合并

###### #召唤术

​		ul>li*5 [tab]

**特殊字符和注释**

实体名称对大小写敏感

![image-20220304105102756](https://cdn.jsdelivr.net/gh/syy404/photospace/202203230954830.png)

注释大全：https://www.w3school.com.cn/tags/index.asp

##### 图片和音视频

- img元素

  </img src= "images/logo.png" alt="一个漏勾" width="x" height="y">

  - img元素为单标签元素

  - src为绝对路径或url（故图像内容不包括在网页中）

  - alt为描述信息
  - width和height为长宽

- audio元素

  - </audio ||:属性=“属性值”></audio>

  - | src      | url        |
    | -------- | ---------- |
    | controls | 音频控件   |
    | loop     | 循环播放   |
    | autoplay | 自动播放   |
    | muted    | 静音       |
    | preload  | 预加载音频 |

  - 支持mp3、ogg、wav

  - source元素指定多个媒体源

    - </audio> <source src="xxx" type="audio/ogg"> <source src="yyy" type="audio/mp3">
      </audio>

- video元素

  - 同上

  - | src          | url                    |
    | ------------ | ---------------------- |
    | width/height |                        |
    | poster       | 封面图，无则默认第一帧 |
    | controls     | 控件                   |
    | autoplay     |                        |
    | loop         |                        |
    | muted        |                        |
    | preload      |                        |

  - 支持mp4、ogg、WebM

#### 元素

**div(sion)**

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

**HTML5**

| 头部：logo&导航          | header  |
| ------------------------ | ------- |
| 导航                     | nav     |
| 独立区块                 | article |
| 划分：内含标题元素       | section |
| 附属信息                 | aside   |
| 页脚：版权信息、联系信息 | footer  |

## ❗CSS

#### 语法

**定义格式**

<style>
    selector{//样式名称	
        property:value;//样式属性&属性值
}
</style>

**单位**

- 绝对单位

1 in = 2.54cm	1 pt = 1/72 in	1 pc = 12 pt 

cm\mm

- 相对单位

| 单位 | 说明                                                  |
| ---- | ----------------------------------------------------- |
| px   | 像素，相对于显示器的屏幕分辨率                        |
| em   | 相对于当前元素的字体大小                              |
| rem  | 相对于默认基础字体的大小，即相对于 html元素的字体大小 |
| %    | 相对于父级元素的百分比                                |

#### 盒模型

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203230954752.png" alt="image-20220313110058734" style="zoom:50%;" />

**margin**    #召唤术：m0 [tab]

| 分开写              | 简写                                 |
| ------------------- | ------------------------------------ |
| margin-top: 0;      | margin: 10px//四个方向               |
| margin-right: auto; | margin: 0 auto;//上下 左右           |
| margin-bottom: 0;   | margin: 0 auto 10px;//上 左右 下     |
| margin-left: auto;  | margin: 10px 20px 30px 40px;//顺时针 |

**padding**    #召唤术：p0 [tab]

| 分开写 | 简写                                |
| ------ | ----------------------------------- |
| 同上   |                                     |
|        | padding: 10px 20px;//上下 左右      |
|        | padding:10px 20px 20px;//上 左右 下 |
|        | 同上                                |

**border**

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203230954068.png" alt="image-20220313111611725" style="zoom:50%;" />

e.g.	border-top: 1px solid #000;

**#border-radius** 圆角边框

衍生：border-top-left-radius;	border-bottom-right-radius

- : 50px;    #4个角为半径50px的圆弧
- :15px 50px;    #左上右下15px，右上左下50px
- :50%;    #圆形
- :height/2;    #胶囊( ﾟ∀ﾟ)

**box-shadow**

| 属性值   | 说明                                                     |
| -------- | -------------------------------------------------------- |
| h-offset | 必需，阴影的水平偏移，允许负值                           |
| v-offset | 必需，阴影的垂直偏移，允许负值                           |
| blur     | 可选，阴影模糊半径，默认为0                              |
| spread   | 可选，阴影扩展半径。正值表示扩大，负值表示 缩小，默认为0 |
| color    | 可选，阴影的颜色，默认黑色                               |
| inset    | 可选，将外部阴影(outset)改为内部阴影                     |

**CSS重置**

#### 颜色

16**进制**

#rrggbb

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203230954642.png" alt="image-20220314182637755" style="zoom:50%;" />

**RGBA形式**

rgba(0,0,0,0)~(255,255,255,1.0)	rgb(0%,100%,0%)

**CSS颜色规范**

147种

**HSLA形式**

色相饱和度用hsl(h,s,l)函数来指定颜色 

− h用来指定色相，其取值范围是0-360 

− s用来指定饱和度，其取值范围是0%-100% 

− l用来表示明度，其取值范围是0%

− a表示透明度，其取值范围为：0.0-1.0

**background-color 前景色**

*建立设计规范*

#### 常用的文本样式

| 文字颜色     | color            |                                   |
| :----------- | ---------------- | --------------------------------- |
| 背景颜色     | background-color | 不可继承                          |
| 字体         | font-family      | 设置多个字体;可以继承             |
| 字号         | font-size        | px                                |
| 加粗方式     | font-weight      | 见下                              |
| 斜体         | font-style       | normal;italic;oblique             |
| 字间距       | letter-spacing   | 1px                               |
| 行高         | line-height      | 2(2倍);32px                       |
| 首行缩进     | text-indent      | 2em（两个相对单位）               |
| 水平对齐方式 | text-align       | left;center;right;justify;inherit |

**Web字体设置**：@font-face规则

```html
@font-face
{
​	font-family: shouxie;
​	src: url("font/FZXingKXJ.OTF");
}#字体定义

p{
	font-family: shouxie;
}
```



<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203230954821.png" alt="image-20220317111924177" style="zoom:50%;" />

![image-20220324115218380](https://cdn.jsdelivr.net/gh/syy404/photospace/202203241152598.png)

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203230954703.png" alt="image-20220317111942493" style="zoom:50%;" />

#### 常用的图像和视频样式

**图像大小**

img{

​	width: 100%;#使宽度与所在容器宽度相同

​	//max-width: 100%;#使宽度与原图像宽相同	

​	height: auto;

}

*video元素同理*

**图像和文字对齐**

| 默认对齐（和基线，存在间隙 | baseline             |
| -------------------------- | -------------------- |
| 垂直顶部对齐（和大写线     | vertical-align: top; |
| 居中（和中线               | middle               |
| 底部（和下缘线             | bottom               |

**背景图像**

- background-image: url("...")
  - url也可以换成
    - linear-gradient(red,yellow)红到黄的线性渐变
    - radial-gradient(red,yellow)红到黄的径向渐变
- background-repeat: 
  - repeat//水平垂直均重复（默认
  - repeat-x//水平重复
  - repeat-y//垂直
  - no-repeat//不重复
- background-position: x y;//数值百分比皆可
  - x
    - left
    - center
    - right
  - y
    - top
    - center
    - bottom
- background-attachment:
  - scroll//随网页一起滚动
  - fixed//固定
- background-size: x//具体值
  - auto//原尺寸
  - contain//完全装进去
  - cover//完全覆盖掉



#### CSS和HTML结合

**内部样式**

​	style元素

**行内样式**

​	网页元素的style属性，即对某个元素单设

​	</p style="font-size:24px">。。。</p>

**外部样式**

​	丢外边，网站内用link元素

​	<link

#### 选择器

​	优先级：

​	行内>ID选择器>类选择器>类型选择器

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203230955362.png" alt="image-20220314184055126" style="zoom:50%;" />

**类型选择器**

header	h1	blockquote	p	footer

```
p{
​	color:#333;
}
```

**类选择器**

`. question{color:#A40000}`

#<p class="question">类样式的使用</p>

**ID选择器**

`#meta_content`

```html
#container{
​	width:677px;
​	margin:0 auto;
}
```

**后代选择器**

=儿子 孙子 重孙子...

`wenda p{text-indent: 0}`

选择selectorA的所有下级selectorB元素

​	`selectorA selectorB`

**子元素选择器**

=儿子

`selectorA>selectorB`

选择selectorA的直接后代selectorB元素

**通配符选择器**

```html
*{
​	margin:0;
​	padding:0
}
```

**伪类选择器**

伪类：pseudo-class

超链接参数

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203261254206.png" alt="image-20220326125417023" style="zoom:50%;" />

​	顺序：LoVe HAte

```html
a:link,a:visited{
	color: #A40000;
	text-decoration: none;
}
```

特定位置参数

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203261255963.png" alt="image-20220326125531867" style="zoom:50%;" />

e.g. p:nth-child(odd)

**伪元素选择器**

- 能够在网页文档中插入额外的元素

![image-20220326131813691](https://cdn.jsdelivr.net/gh/syy404/photospace/202203261318797.png)

## 移动端

**视口**

<meta name="viewport" content="width=device-width,initial-scale=1">
</meta>


**max-width**

设置以避免进一步扩大

**padding**

留白

## 超链接

~~link startt!!~~

### anchor

</a href="路径" target="连接目标在何处打开">title</a>

**herf**

- 绝对路径 url
- 相对路径 /xxx/yyy.html
- 锚点 #top    回到顶部
- 电子邮件 sysmail@mail.com

- 空链接 #

**target**

- 打开链接 _self
- new tab打开链接 _blank

