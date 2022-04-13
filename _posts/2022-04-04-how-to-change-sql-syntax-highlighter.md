---
layout: post
title: syntax highlighter
date: 2022-4-4
author: 笨比sy
tags: [CSS, Newbie]
comments: false
toc: true
pinned: false
layout: post
---

唉
在上一次大修blog的时候就对code font嗤之以鼻，真的很难理解为什么会有人喜欢看这种字体的代码，高亮也加的很奇怪，除了一股文艺风真的毫无可读性。所以打算自己动手去解决一下这件事。

原本以为只是修个CSS文件的事，没想到低估了问题的复杂程度~~sy菜的程度~~，硬是研究了老半天，进展极其缓慢。虽然最后还是弄出来了，不过在这里总结一下自己的经验教训，希望以后在面对问题的时候能够快一点。

<!-- more -->

## 需求

果然做事情首先要明确需求：

- 修改code font
- 统一颜色风格
- 加入对SQL语句的高亮支持

## 进程

### 字体修改

第一件事的解决路上就碰到了问题。我不是很能看得懂文件之间的互相引用关系，不过好在花了一些事件之后还是能够理顺结构的，很顺利地找到了code font，并且修改为了自己认为比较美观的字体。

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202204042250974.png" alt="image-20220404225026845" style="zoom:50%;" />

修改前↑ 字体为Menlo

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202204042251176.png" alt="image-20220404225129097" style="zoom:50%;" />

修改后↑ 使用了Source Code Pro，个人认为可读性大增加

~~代码用什么衬线啊~~

至此，blog一下子就顺眼了很多

### 颜色风格

我并没有去直接找开源的highlight方案，而是就着手上的Typora Theme挑了一个自己喜欢的，然后按照里面的配色方案对blog进行修改。至于为什么，可能只是觉得Typora的配色就已经足够好了吧。

但是在着手修改的时候遇到了大问题，那就是对于代码的分类，两个软件使用的类名是不一样的。我只能根据注释进行大致的对照，但由于~~本人英语水平过蒻~~对代码语法的具体名称不是很熟悉，所以只实现了大概的对照。

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202204042301667.png" alt="image-20220404230130523" style="zoom:50%;" />

←左边是Notion方案，右边是JekyII的方案，分得更细→

### SQL语句的高亮支持

这里真的花了很多很多时间，由于走在了错误的路上。

想到的第一个方法是找到这些类的定义，加入对SQL代码的定义并且回到highlight.css文件设置。

我最开始以为对code类的定义是在项目中有的，所以把每一个文件都细细看了一遍，结果发现并没有类似的东西(;´Д`)

所以我将这个方案暂放在了一边，开始寻思如何在自己的项目里面加插件……后来发现插件是全局的，前面的设置都会被覆盖掉，觉得很不甘心。今天下了狠心决定自己解决这个问题，Google了一大圈，首先找到了这个👇

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202204042308401.png" alt="image-20220404230837276" style="zoom:50%;" />

https://highlightjs.org/

我靠，要是早点让我知道还有这玩意我就不用大费周章做这些事了( ・_ゝ・)

又是一刻钟高强度搜索，好久没看英语再加上专业词汇不熟悉，脑袋看得生疼。不过最终功夫不负有心人，我找到了这位佬的blog👇

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202204042311133.png" alt="image-20220404231111041" style="zoom:50%;" />

https://www.angularfix.com/2021/12/how-to-modify-syntax-highlighting-in.html

最后终于摸到了这里

https://github.com/rouge-ruby/rouge

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202204102030400.png" alt="image-20220407200620169" style="zoom:33%;" />

这是JekyII所使用的Rouge Highlighter，能够找到所有相关的定义文档。同时，也可以在这个网站中找到Rouge的各种主题支持👇

https://github.com/brazacz/rouge-themes

### 总结一下

- sy是笨蛋
  - 对技术相关的词库真的了解得太少了，以至于在面对满屏的英语时很多关键词都不知道是在说什么，阅读很多技术向blog的时候都非常艰难，在这方面对中文的依赖性还是没有降下来，经此一事值得警醒。
- 花心
  - 查着查着就跑偏了。比如明明是查JekyII的CSS规范，结果对着Ruby的开发文档看了很久(;´ヮ`)7
  - 总想换车。谁能想到因为这样一件事（当然还有和tg同步）我开始认真思考要不要转到wordpress去，不过后来还是决定自己折腾Jekyll，股哦然还是享受自己开发的过程……虽然总是贪心想着自己造轮子。
- 技术方面的不足
  - 对开源项目的运作还是不熟悉，没有善用正确的搜索工具，也没有朝着最佳方向去搜索

## 最后碎碎念

最近折腾blog也不是一天两天了。现在经常性地对着一堆我不熟悉的专业名词硬着头皮读下去，至于吸收了多少恐怕只有天知道( ・_ゝ・)

同步blog和微信公众号还是挺简单的一件事情，唯一需要在意的就是发还是不发。而且我估计一些内容应该是不能在公众号里发的吧？之后应该会采取blog长文+channel日常+公众号同步~~引流~~的模式。

下一步果然还是想在blog中实现对telegram channel的抓取，两边同步更新。其实我是相当喜欢tg的，channel更新得比朋友圈什么的多多了（半个猫猫频道）

所以最后在这里打个广告吧，欢迎关注我的channel！

https://t.me/prejudices404

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202204072025144.png" alt="image-20220407202526031" style="zoom: 67%;" />

顺便放一个公众号在这里，虽然还没有开始运营(;´ヮ`)7

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202204072051800.png" alt="image-20220407205022062" style="zoom: 80%;" />