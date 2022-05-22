---
layout: post
title: 💦PostgreSQL
date: 2022-05-22
author: 笨比sy
tags: [PostgreSQL,Newbie,Linux]
comments: false
toc: true
pinned: false
---

Password：114514

师爷您给翻译翻译？

<!-- more -->

## 安装postgres

> 首先解释一下，这里的安装步骤适用于Linux系统。
>
> *【Linux系统】是与Windows、MacOS等平行的操作系统，特点是输入文字命令进行控制，而不是如同Windows的逻辑一般，将所有的操作都封装成为一个个的按钮。*
>
> 我们在虚拟机打开的【终端】**可以理解为**~（虽然并不是）~Windows系统中所用的【cmd】或【powershell】，它能够理解你按照一定语法输入的命令，并且执行。
>
> 在Linux系统中，几乎所有的操作都通过【输入指令】来完成。
>
> 这些知识将有助于对安装步骤和后续操作的理解。

1】sudo：调用管理员权限

`sudo apt install postgresql`

​		apt：Linux下的一个安装包管理工具，在这里可以理解为一个下载器，你将通过这个东西下载【postgresql】这个软件

2】启用

`sudo service postgresql start`

3】查询状态是否为online

`service postgresql status`

​	此时实际上创建了一个专门的账号postgres，输入exit退回

4】清空原有密码并重新设置

`sudo passwd -d postgres`

`sudo -u postgres passwd`

~~`114514`~~

​	-u：作为“postgres”这个用户执行后面的操作

5】登录账户

`su postgres`

6】进入postgres

`psql` 或 `sudo -u postgres psql`

`psql` 是postgres的命令行程序，在Linux中输入该命令以运行postgres

#】卸载postgreSQL

`sudo apt remove postgresql*`

## 控制命令

> Linux有一点不好就在于它不直观，容易绕晕。这里列出每一层会显示的以便操作中查阅自己到了哪里，就以蓝桥虚拟机为例。
>
> `shiyanlou:~/ $`	最底层，可以理解为桌面，可以通过
>
> `postgres@7be05fld90c4:/home/shiyanlou$`	输入 `psql` 即可进入postgres
>
> `postgres=#`	postgres 的主界面
>
> `postgres-#`	没打分号，打分号以结束命令
>
> ​		`光标处为空的查询界面`	特征是只能上下翻页，按 `q` 来退回到可操作的**命令模式**
>
> ​		`自定义名=#`	用了 `\c 数据库名` 命令进入到了该自定义数据库内，用 `exit` 或 `quit` 退回
>
> 

- Linux操作命令
  - ⚠命令对大小写敏感
  - ctrl+f、ctrl+b或U(p)、D(own)上下翻页、
  - home、end键跳转页首/页尾
  - :q 退出当前内容
  - \h +具体命令 查看具体使用
  - :! 强制命令
    - 当出现no written 警告，可使用`:!q`强制退出
  - :w 保存
    - :wq 保存并退出
- postgres操作命令
  - \c 进入【后接数据库名】
  - \l 查数据库
  - \d 查表
  - 中括号内是可以省略的内容
    - [IF EXISTS] 会执行判断，判断不通过会继续程序而不是直接停止

<!--o老师的腾讯云地址101.34.176.155-->

<!-- ssh postgres@101.34.176.155-->

## postgres使用

绝大多数与mySQL查询语句相同，此处仅列出**最简语句**。

mySQL语句基础参见：https://syy404.github.io/discoelysium/mySQL/

##### 插入数据

```mysql
INSERT INTO(column1,column2) 
	VALUE('x','y');
```

##### 删除数据

```mysql
DELETE FROM table1；
```

##### 更新数据

```mysql
UPDATE table1
SET x='newx'
```

##### 关系模型

- 竖着的列(column)
  - 被称作属性(attribute)
  - 属性是没有次序的
- 横着的行(row)被称为
  - 元组(tuple)
  - 记录(record)
- 行和列构成的
  - 是一个关系(relation)

##### 导入文件

> 首先你得创建一个文件对吧？
>
> **创建文件**
>
> 1】建立文件 `vi 路径`
>
> eg：`vi /tmp/test.sql`
>
> ​		更多关于 `vi` 命令的介绍可以查看https://www.runoob.com/linux/linux-vim.html
>
> 2】按 `i` 进入对文件的**编辑**
>
> ​		注意这里是输入**操作命令**而非**文件内容**
>
> 3】输入 `:w` 来保存
>
> 4】`esc`退回

在postgres中输入命令：`\i /tmp/test.sql`插入表格

#`sudo -u postgres psql -f '/tmp/test.sql'`能够直接执行上述操作

​	很明显，这一句话是由几个命令拼起来的，它基本相当于windows中的【右击选中文件，将文件导入到postgres】



## Tomcat使用

~~你问也不知道，咱也不懂，总之是被蓝桥虚拟机拦下来了，G~~

==I DID IT!== 把油猴关了之后就让我过了ᕕ( ᐛ )ᕗ

### 安装

1】下载tomcat到本地

`git clone https://gitee.com/overmind1980/tomcat10.git`

​	#】将tomcat复制到opt中

​	`cp -r apache-tomcat-10.0.12 /opt/`

​	`ls /opt`	进入opt文件夹

2】进入tomcat

`cd tomcat10`

`tar -zxf apache-tomcat-10.0.12.tar.gz`

`cd apache-tomcat-10.0.12/`

3】进入bin，打开tomcat（**本步也是对服务器的启动命令）**

此处前缀应是`ID:apache-tomcat-10.0.12/(main*)$`

`cd bin`

`sudo ./startup.sh`	在bin文件下启动服务器

**Tomcat started!**

### 建构动态网页

查阅Tomcat的要求后，发现这样一个网页需要有基本的结构。

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202204261645494.png" alt="image-20220426163418321" style="zoom:33%;" />

O老师主要纠结的地方也在这里，那就开始罢（悲）

https://www.lanqiao.cn/courses/2712/learning/?id=260421

### 基本操作

`..`	退回上一层

`mkdir 名字 `	建立文件夹

`cd 名字`	进入文件夹

`echo+"内容">文件名` 	创建一个文件、且输入了内容

`rm -rf 文件名`    删掉文件

`cp 名字 ./` 	复制	**请严格遵守语法，文件后打一空格再加上./**

`javac`	编译java文件

`vi 文件名`	编辑某个文件

`tab` 可以自动补齐文件或文件夹名

#### tmux操作

输入 `tmux` 进入tmux辅助（最下面的绿色条条

`ctrl+b` `c` 建立新的窗口

`ctrl+b` `,` 重命名窗口

### 其他操作

在网页中

<img src="https://cdn.jsdelivr.net/gh/syy404/photospace/202205101412581.png" alt="image-20220510141202478" style="zoom:33%;" />

所以是可以直接改wd=后面的字符进行直接搜索（注意下一个内容以&开头）

同理对 `s?q=` 后的字符也可以进行类似的操作
