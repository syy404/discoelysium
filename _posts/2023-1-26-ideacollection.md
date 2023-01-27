---
layout: post
title: question collection
date: 2023-01-26
author: 笨比sy
tags: [C++, Newbie]
comments: false
toc: true
pinned: false
---

日进一寸。

<!-- more -->

## 数组

### 最大最小值、和

```c++
//已知数组内容范围为0~5000
int max = 0;
int min = 5001;
for(int i = 0; i < n; i++){
            scanf("%d", &a[i]);
            if(a[i] > max) max = a[i];
            if(a[i] < min) min = a[i];
            sum += a[i];
        }
```

## 输出

【double=0施工中】

### 字符

```c++
char a;
int num = c-'A'+1;
for(char b = "A"; b<= 'A'+i-1; b++){
    printf("%c", b);
}
```

如果a是一个数字，会自动转换成ascii码，可以进行以上操作。

## 循环

### 无限循环

```c++
while(1){};
for(;;);
```

### 持续输出

```c++
while(scanf("%d", &n) != EOF){}
while(~scanf("%d", &n)){}
```

while(~x)

while(~x)的意义在于按位取反

## 运算

### 除法 /

参与运算的量均为整型时，结果为整型（舍去小数）

求余符号的正负取舍与被除数符号相同

```c++
5 / 2 = 2;
1 / 2 = 0;
-3 /16 = 0;
16 / -3 = -5;
```

### 求余 %

要求两个操作数均为整型并发生隐式转换

```c++
5 % 2 = 1;
1 % 2 = 1;
-3 % 16 = -3;
16 % -3 = 1;
```

## 型

### 开float还是double

经验：开float的都大失败( ﾟ∀。)7''
