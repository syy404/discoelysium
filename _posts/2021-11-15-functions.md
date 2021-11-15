---
layout: post
title: 函数垃圾箱
date: 2021-11-15
author: 笨比sy
tags: [C++, Newbie]
comments: false
toc: true
pinned: false
---
有用没用见到的函数都在这里
为什么不自己背啊笨蛋( `д´)

### 函数！

#### 自我定义

```c++
返回值类型 函数名(参数1类型 参数1名称,参数2类型 参数2名称) 

{ 
语句组(函数体); 
返回值; 
}
```

通常定义在main函数外

函数不允许嵌套定义

**return**语句的功能是**结束函数的执行，并将**“**返回值**”**作为函数的结果返回**。“返回值”可以是常量，变量或者复杂的表达式等。

函数的返回值类型还可以是**void**，表示函数没有返回值，可以不写**return**,也可以写**return** **；**作为函数的结束。

```c++
int a[]={1,3,5,7,9,11,13}; 
void print(int n){//输出a数组的前n个数 
for(int i=0;i<n;++i) 
printf("%d ",a[i]); 
return ; 
}
```

自定义函数能让你少写很多东西，免得把时间浪费在重复的工作上



#### 函数参数的传递

##### 传值调用

将实参的数据值传递给形参，不改变实参

```c++
void swap(int a,int b){ int c=a; a=b; b=c; }
```



#### 处理字符组的函数

| 1    | **strcpy(s1, s2);** 复制字符串 s2 到字符串 s1，参数可以为字符串数组，以及字符串 |
| ---- | ------------------------------------------------------------ |
| 2    | **strcat(s1, s2);** 连接字符串 s2 到字符串 s1 的末尾。连接字符串也可以用 **+** 号 |
| 3    | **strlen(s1);** 返回字符串 s1 的长度。                       |
| 4    | **strcmp(s1, s2);** 如果 s1 和 s2 是相同的，则返回 0；如果 s1<s2 则返回值小于 0；如果 s1>s2 则返回值大于 0。该函数的参数可以*是指针、字符串常量或者字符数组名。* |
| 5    | **strchr(s1, ch);** 返回一个指针，指向字符串 s1 中字符 ch 的第一次出现的位置。 |
| 6    | **strstr(s1, s2);** 返回一个指针，指向字符串 s1 中字符串 s2 的第一次出现的位置。 |



#### 数学函数

| 序号 | 函数 & 描述                                                  |
| :--- | :----------------------------------------------------------- |
| 1    | **double cos(double);** 该函数返回弧度角（double 型）的余弦。 |
| 2    | **double sin(double);** 该函数返回弧度角（double 型）的正弦。 |
| 3    | **double tan(double);** 该函数返回弧度角（double 型）的正切。 |
| 4    | **double log(double);** 该函数返回参数的自然对数。           |
| 5    | **double pow(double, double);** 假设第一个参数为 x，第二个参数为 y，则该函数返回 x 的 y 次方。 |
| 6    | **double hypot(double, double);** 该函数返回两个参数的平方总和的平方根，也就是说，参数为一个直角三角形的两个直角边，函数会返回斜边的长度。 |
| 7    | **double sqrt(double);** 该函数返回参数的平方根。            |
| 8    | **int abs(int);** 该函数返回**整数**的绝对值。               |
| 9    | **double fabs(double);** 该函数返回任意一个**浮点数**的绝对值。 |
| 10   | **double floor(double);** 该函数返回一个小于或等于传入参数的最大整数。*高斯函数* |
| 11   | **double ceil(double);**返回一个大于等于                     |

#### 输入输出函数

scanf\printf

cin

```c++
cin.getline(name,20);//读入一行，通过换行符来确定行尾，最后将换行符改为空字符；19表示你将最多读入19个字符，最后一个必为空字符
cin.get(name,arsize);//get将换行字符留在输入队列中
```



string.h中定义的函数

| 1    | void *memchr(const void *str, int c, size_t n)在参数 *str* 所指向的字符串的前 n 个字节中搜索第一次出现字符 c（一个无符号字符）的位置。 |
| ---- | ------------------------------------------------------------ |
| 2    | int memcmp(const void *str1, const void *str2, size_t n)把 *str1* 和 *str2* 的前 n 个字节进行比较。 |
| 3    | void *memcpy(void *dest, const void *src, size_t n) 从 src 复制 n 个字符到 *dest*。 |
| 4    | void *memmove(void *dest, const void *src, size_t n)另一个用于从 *src* 复制 n 个字符到 *dest* 的函数。 |
| 5    | void *memset(void *str, int c, size_t n)复制字符 c（一个无符号字符）到参数 *str* 所指向的字符串的前 n 个字符。 |

注：这里的void是不需要打的（

