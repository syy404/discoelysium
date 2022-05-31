---
layout: post
title: 🐒HTML入门(更新到CSS布局)
date: 2022-05-24
author: 笨比sy
tags: [HTML,Newbie]
comments: false
toc: true
pinned: false
---

救世啊⚠本文为防止markdown自动吃掉HTML代码，在部分元素声明前多加了一道斜杠，参考时请去除食用（

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203231152182.png" alt="image-20220323115253921" style="zoom:10%;" />

<!-- more -->

## 语法和结构

#### 属性

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203230954244.png" alt="image-20220303113305854" style="zoom: 50%;" />

#### 大小写

本学期建议大家在编写网页时注意以下准则，避免出现语法错误：

‒ **标签名和属性名称小写** 

‒ 所有属性都放在开始标签的尖括号内。

‒ 标签名称和属性之间以及不同属性之间都用空格分隔 

‒ 属性值放在属性之后，用等号分隔

‒ 属性值应该被包含在英文双引号中

#### 基本结构

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203230954532.png" alt="image-20220303113750165" style="zoom:33%;" />

**meta**

-定义HTML文档的编码格式，在HTML5之后变得简洁

​	meta charset

-用于提供与浏览器或者搜索引擎的相关信息

​	meta name

###### #召唤术

​	`meta:vp	[tab]`

**link**

-用于引入其他的文件，如CSS文件和显示在浏览器标题/收藏夹的图标

#### 语法

##### 文字   

- **p**

- em

​		`</em>文字</em>`

- strong

​		`</strong>文字</strong>`

- span

​		对元素进行区隔使其以不同样式显示（不具有任何样式，需要结合CSS

​		`</span>段落文字</span>`

- br

​		段内换行，使后面的内容显示于下一行，无空行（仍属于同一段落）

​		`文字</br>文字`

- sup/sub

​		上标superscript，下标subscript

​		`</sup>文字</sup>//上标`

​		`</sub>文字</sub>`

- blockquote

块引用，默认为左右两侧缩进

`</blockquote>引用的文字</blockquote>`

- pre

代码块，保留空格和换行符

`</pre>文字   文字</pre>`

###### #召唤术

​	`lorem字数 [enter]`

**list**

- ul

​		无序列表unordered list 

​		`</ul>`
`​    		<li>list 1</li>`
`​    		<li>list 2</li>`
`​		</ul>`


- ol

​		有序列表ordered list

​		`</ol>`
`​			<li>list 1</li>`
`​			<li>list 2</li>`
`​		</ol>`


​		type可以是A/a/I/i/1

- dl

​		定义列表definition list

​		`</dl>`
`​			<dt>definition term</dt>`
`​    		<dd>definition description</dd>`
`​		</dl>`

**表格**

​		`</table>`
`​    		<caption>title</caption>`
`​    		<tr>`
`​        		<th>table header1</th>`
`​        		<th>table header2</th>`
`​    		</tr>`
`​    		<tr>`
`​        		<td>table data1</td>`
`​        		<td>table data2</td>`
`​    		</tr>`
`​		</table>`


​		tr=table row

​		thead=表格头部信息

​		tbody=表格主体信息

​		tfoot=表格页脚信息

​		colspan=跨列合并

​		rowspan=跨行合并

###### #召唤术

​		`ul>li*5 [tab]`

**特殊字符和注释**

实体名称对大小写敏感

![image-20220304105102756](https://cdn.jsdelivr.net/gh/syy404/photospace/202203230954830.png)

注释大全：https://www.w3school.com.cn/tags/index.asp

##### 图片和音视频

- img元素

  `<img src= "images/logo.png" alt="一个漏勾" width="x" height="y">`

  - img元素为单标签元素

  - src为绝对路径或url（故图像内容不包括在网页中）

  - alt为描述信息
  - width和height为长宽

- audio元素

  - `<audio ||:属性=“属性值”></audio>`

  - | src      | url        |
    | -------- | ---------- |
    | controls | 音频控件   |
    | loop     | 循环播放   |
    | autoplay | 自动播放   |
    | muted    | 静音       |
    | preload  | 预加载音频 |

  - 支持mp3、ogg、wav

  - source元素指定多个媒体源

    - `<audio> <source src="xxx" type="audio/ogg"> <source src="yyy" type="audio/mp3">`
      `</audio>`

  - 常用设置

    - ```css
      audio{
      	width:100%;
      }
      ```

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

  - 常用CCS设置

    - ```css
      video{
      	max-width:100%;
      	height:auto;
      }
      ```

- iframe元素

  - 通用代码，适于嵌入分享元素

  - 默认为300*150大小

  - 更改后

    ```html
    <iframe frameborder="0" width="750" height="420" src="https://v.qq.com/txp/iframe/player.html?vid=k3019m7iwlk" allowFullScreen="true">
    </iframe>
    ```

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

```css
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

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203241152598.png" alt="image-20220324115218380" style="zoom: 50%;" />

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203230954703.png" alt="image-20220317111942493" style="zoom:50%;" />

#### 常用的图像和视频样式

**图像大小**

```html
img{
width: 100%;#使宽度与所在容器宽度相同
//max-width: 100%;#使宽度与原图像宽相同	
height: auto;
}
```

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

​	<p style="font-size:24px">。。。</p>

**外部样式**

​	丢外边，网站内用link元素

​	<link

#### 选择器

​	优先级：

​	行内>ID选择器>类选择器>类型选择器

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203230955362.png" alt="image-20220314184055126" style="zoom:50%;" />

**类型选择器**

header	h1	blockquote	p	footer

```css
p{
​	color:#333;
}
```

**类选择器**

`. question{color:#A40000}`

#<p class="question">类样式的使用</p>

**ID选择器**

`#meta_content`

```css
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

```css
*{
​	margin:0;
​	padding:0
}
```

**伪类选择器**

伪类：pseudo-class

超链接参数

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203261254206.png" alt="image-20220326125417023" style="zoom: 33%;" />

​	顺序：LoVe HAte

```css
a:link,a:visited{
	color: #A40000;
	text-decoration: none;
}
```

特定位置参数

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203261255963.png" alt="image-20220326125531867" style="zoom: 33%;" />

e.g. p:nth-child(odd)

**伪元素选择器**

- 能够在网页文档中插入额外的元素

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202203261318797.png" alt="image-20220326131813691" style="zoom:33%;" />

#### CSS对块元素操作

`display:none;` 把块收起来

`visibility:hidden；` 让块看不见

`opacity:0; #0为全透明，1为不透明` 更改透明度

##### 居中

- 块级元素：`margin: 0 auto;`
- 行内元素：`text-align:center;  #使块级元素中的所有行内元素居中`

##### 内容溢出

设置`overflow`属性

| visible | 允许溢出           |
| ------- | ------------------ |
| hidden  | 隐藏溢出内容       |
| scroll  | 滚动条常显         |
| auto    | 在溢出时显示滚动条 |

#overflow案例

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202204281059298.png" alt="image-20220428105954231" style="zoom:33%;" />

## 理论对接

### 移动端适应

**视口**

<meta name="viewport" content="width=device-width,initial-scale=1.0">
</meta>//设置当前接口的宽度为设备宽度，同时页面的初始缩放值为1.0

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202205191117209.png" alt="image-20220519111747156" style="zoom:50%;" />

- 设备像素比DPR：物理像素 / 逻辑像素
- 对高分辨的设备，需要为它准备更多像素的图像，在设计领域被称 为2倍图、3倍图，文件名称中会包含@2x、@3x这样的标识

**max-width**

设置以避免进一步扩大

**padding**

留白

### 媒体查询

属于CSS属性

1. 内部样式

   ```css
   @media mediaType and (mediaFeature){
   	...
   }
   ```

2. 外接

   ```css
   <link rel="stylesheet" media="mediaType and (mediaFeature)" href="stylesheet.css">
   ```

**media type**

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202205191127476.png" alt="image-20220519112734422" style="zoom:50%;" />

**media Feature**

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202205191128156.png" alt="image-20220519112806108" style="zoom:60%;" />

还有max-width和min-width

**断点**

注意按照<u>宽度止从小到大</u>的规律书写

```css
CSS样式;/*576px以下的样式*/
@media (min-width: 576px) {CSS样式}/*小型终端(landscape phones, 576px 及以上)*/
@media (min-width: 768px) {CSS样式}/*中型终端(tablets, 768px及以上)*/
@media (min-width: 992px) {CSS样式}/*大型终端 (desktops, 992px及以上)*/
@media (min-width: 1200px) {CSS样式}/*超大型终端(large desktops, 1200px及以上)*/
```

**响应式设定**

使图像、视频等随所在容器自动缩放

```css
img { 
    width: 100%; 
    height: auto;
}
/*两种方法,video同理*/
img { 
    max-width: 100%; 
    height: auto;
}
```



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

## 布局

### 审美

首先要建立起正确的审美观念，个人觉得这还挺重要的。

本节为个人锐评(=ﾟωﾟ)=

1. 黄金分割

   ![image-20220524154939901](https://cdn.jsdelivr.net/gh/syy404/photospace/202205241549105.png)

   案例是推特的。这样的布局比较适合简单排版，但是对富文本的呈现并不算太友好，可塑性也不高，不是很喜欢（

2. 面包屑导航<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202205241553693.png" alt="image-20220524155305635" style="zoom:33%;" />

3. 标签：不要小瞧了tag，这是现在挺火的多形式呈现（不会说）模式的中心，notion飞书文档什么的都在用

4. 焦点图：参考公众号头图

5. [卡片式](https://dribbble.com/)：个人比较喜欢的排版，灵活多变，适合复杂的排版和网页模式

6. 图文列表：最基础的图文排布格式，不会出错，非常严谨

   - 实现：图片 `float:left`；文字 `float:right`；整体: `flex`


老师提供了以960p/980p为标准的基本布局，可以参考。其实基本布局也能玩出花来，只要人有好的审美和设计(｀･ω･)

![image-20220524164845717](https://cdn.jsdelivr.net/gh/syy404/photospace/202205241648800.png)

![image-20220524164908764](https://cdn.jsdelivr.net/gh/syy404/photospace/202205241649825.png)

![image-20220524164932580](https://cdn.jsdelivr.net/gh/syy404/photospace/202205241649669.png)

### 文档流 flow

从上至下的顺序依次展现的流派，默认显示规则

#### 块类型

| 块类型                    | 默认宽度 | 是否允许同行 | 是否允许设定边距   | 是否允许设定宽高 |
| ------------------------- | -------- | ------------ | ------------------ | ---------------- |
| 块级元素 block            | 父元素宽 | N            | 内边距、外边距     | Y                |
| 行内元素 inline           | 内容宽   | Y            | 内边距、左右外边距 | N                |
| 行内块级元素 inline-block | 内容宽   | Y            | 内边距、外边距     | Y                |
| 不显示 none               | /        | /            | /                  | /                |

#### 文档中的margin的合并

当一个元素出现在另一个元素上时，上元素的[margin-bottom]和下元素的[margin-top]会发生合并，仅剩[margin-bottom]

### 浮动 float

浮动元素可以根据实际情况来移动

- 进行图文环绕效果
- float元素不再属于文档流；优先float的移动，常规元素长度改变为float元素留出空间
- 外侧必须有一个container（或div
- margin不合并

`float:left;    #向container的最左侧运动`

#### 常规设定

为避免<u>container失去高度</u>和<u>后续元素入侵container</u>↓

1. 设置父元素CSS属性`overflow:hidden;`迫使父元素包含浮动子元素（超出部分会被隐藏）

2. 在父元素后增加（平级的）空元素以实现阻断和恢复

   - 一般使用CSS属性`clear: both;`
   - <img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202204280953876.png" alt="image-20220428095338763" style="zoom: 33%;" />

3. 设置伪元素选择器，动态增加空的子元素

   - ```css
     .clearfix:after{
     	content:".";
     	display:block; 
     	height:0; 
     	visibility:hidden;
     	clear:both;
     }   /*在CSS中增加这个属性，注意一个元素设定多个class的语法为class="A B"*/
     ```

   - 在浮动盒子中设置 `<div id=“container” class=“clearfix”>……</div>`

### 位置定位 position

position

| static   | 默认                                                         |
| -------- | ------------------------------------------------------------ |
| relative | 基于原位置移动，通过top,bottom,left,right设定；预留位置不变，其它元素位置不变 |
| absolute | 基于最接近、属性为非static的祖先元素或浏览器窗口定位；脱离文档流，浮在网页上面；通过z-index属性控制堆叠顺序；坐标原点通过top,bottom,left,right设定 |
| fixed    | 以浏览器窗口为基准定位，不跟随滚动                           |

#关于absolute设定举例

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202204281052611.png" alt="image-20220428105236532" style="zoom: 50%;" />

#关于fixed设定举例

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202204281059239.png" alt="image-20220428105713322" style="zoom: 33%;" />

### 弹性 Flex

flex布局所有子元素自动成为容器成员（flex item，或弹性元素）

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202205191149786.png" alt="image-20220519114915736"  />

弹性元素可以在任何方向上排布，也可以弹性伸缩尺寸；既可以增加尺寸以填满未使用的空间，也可以收缩尺寸以避免从弹性容器溢出

#### 对Flexbox

- flex-direction：设置主轴的方向
  - row（默认值）：主轴为水平方向，起点在左端
  - row-reverse：主轴为水平方向，起点在右端
  - column：主轴为垂直方向，起点在上沿
  - column-reverse：主轴为垂直方向，起点在下沿
- flex-wrap：设置如果一行轴线排不下所有的flex项目，如何换行
  - nowrap（默认）：不换行
  - wrap：换行，第一行在上方
  - wrap-reverse：换行，第一行在下方
- justify-content：设置如何分配<u>沿着flex容器主轴的flex项目</u>之间及其周围的空间
  - flex-star：flex项目从行首位置开始排列，为默认值
  - flex-end：flex项目从行尾位置开始排列
  - center：flex项目居中排列
  - space-between：flex项目平均地分布在行里。每行第一个元 素排列在行首，每行最后一个元素排列在行尾
  - space-around：flex项目平均地分布在行里，每个元素周围分
    配相同的空间
  - <img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202205191202499.png" alt="image-20220519120251449" style="zoom:70%;" />
- align-items：设置flex项目在flex容器侧轴上的对齐方式
  - flex-start：flex项目从侧轴起始位置开始排列
  - flex-end：flex项目从侧轴终点位置开始排列
  - center：flex项目在侧轴居中排列
  - stretch：flex项目拉伸填充整个容器，为默认值
  - <img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202205191210998.png" alt="image-20220519121048947" style="zoom:50%;" />

#### 对Flex item

- flex-basis：设置flex项目在主轴方向上的初始大小

- flex-grow：设置flex项目在flex容器剩余空间中的扩展比率,默认值为0

  - <img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202205191210843.png" alt="image-20220519121014785" style="zoom:60%;" />

- flex-shrink：设置flex项目宽度的总和超出flex容器的时候，在超出的空间（负的 剩余空间）中的收缩比率,默认值为1

  - <img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202205191330176.png" alt="image-20220519133004121" style="zoom:50%;" />

- 以上项目可以用flex标签简写

  - ```css
    .item{
        flex:0 1 auto;/*grow shrink basis*/
    }
    ```

### Grid
