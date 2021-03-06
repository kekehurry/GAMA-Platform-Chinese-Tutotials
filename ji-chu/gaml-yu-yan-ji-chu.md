---
description: >-
  GAML语言是GAMA平台使用的一种面向代理的编程语言，其基本构架与面向对象的编程语言JAVA类似，两者有许多共通之处，GAML语言在JAVA的技术上实现了一系列方便进行模拟的代理功能，如族、代理技能等等
---

# GAML语言基础

### 基本数据类型

GAML的基本数据类型 有**整数int 、浮点数float、字符串string**和**布尔值bool**四种。除了基本数据类型，GAML还内置了一系列图形类型（如**geometry**、**point** 、**path** 、**topology**等\)、集合类型（如**pair**、**list**、**matrix**、**map**等）以及代理类型（如**agent**、**species**等\)。同时GAML还支持使用关键字type，在代理族**species**中自定义不同的类型。更多关于数据类型的内容可以参考[官方文档](https://gama-platform.github.io/wiki/DataTypes)。

### 变量

在GAML语言中，声明一个变量需要显式的声明变量的数据类型+数据名。在GAMA窗口右下角的交互式命令行输入以下命令并查看其输出：

```text
string text;                // 在GAML中'//'是注释，表示其后的内容不会被认为是代码                                               
text -< 'Hello World';      // '-<'是赋值操作，
int a -< 3;                 // GAML每一行代码都以';'结束
float b -< 4;               // GAML会对基础数据类型进行自动转换
bool c -< a=b;              // GAML中'='是判定是否相等，不是赋值
write(c);                   // 不在交互式命令行窗口时，可用write来输出变量的值
```

### 列表、矩阵与字典

GAML中，关键字list表示列表，列表可以直接显式地声明列表中的数据类型，也可以声明列表中的数据类型来构建一个多数据类型的列表。

```text
 list<int>  l_1 <- [5,4,9,8];     //此时要求列表中所有元素都是整数
 list l_2 <- [4,5,'o','j',[1,2]]; //此时列表中元素有不同的数据类型 
 int i <- length(l_1);            //返回列表长度
 string s <- l_2[2];              //返回l_2列表第三个元素
```

GAML中，matrix表示一个二维矩阵或者一个一维向量。

```text
matrix mat1 <- matrix([1,2,3,4,5]);   //通过matrix函数将列表转换为一维向量
matrix mat2 <- 0.0 as_matrix({10,5}); //构造一个10列5行的二维数组，其初始值为0
matrix mat3 <- matrix([[1,2,3],[4,5,6]]); //构造一个2列3行的二维数组
int a <- mat3[0,0];                 //返回mat3矩阵第1列第1行的元素              
```

GAML中，map表示一个存贮键\(key\)-值\(value\)对的字典，在字典中的每一对都表示为`key::value` 。

```text

```

### 数学运算

### 逻辑运算

### 条件语句

### 循环语句



