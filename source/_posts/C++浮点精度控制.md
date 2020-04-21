---
title: C++浮点数精度控制
date: 2020/4/14
tags: 
- C++
categories: C++题目
---

C++浮点精度

<!-- more -->

### C++浮点数精度控制

```
#include<iomanip>
...
cout<<setiosflags(ios::fixed);  //保证setprecision()是设置小数点后的位数。
cout<<setprecision(2) << pi << endl;    //输出3.14
cout<<pi<<endl; //输出3.14
```
<!-- more -->

- 相关知识  
流输入输出也可以进行格式控制， C++ 中是通过流操纵算子来实现的。流操纵算子是在头文件 iomanip 中定义的，因此要使用这些流操纵算子，必须包含该头文件。


```
// 包含流操作算子库
#include <iomanip>
```

C++ 的 iomanip 库提供了多种流操纵算子，来实现不同的格式控制功能，包括设置域宽、设置精度、设置和清除格式化标志、设置域填充字符、在输出流中插入空字符、跳过输入流中的空白字符等，下表为一些常用的流操作算子：


流操纵算子 | 功能描述
---|---
setbase(b) | 以进制基数 b 为输出整数值
setprecision(n)|	将浮点精度设置为 n
setiosflags(long)|	设置特定的格式标志位
setw(n)	| 按照 n 个字符来读或者写
setfill(ch) |	用 ch 填充空白字符
flush |	刷新 ostream 缓冲区
ends |	输出空字符
endl |	输出换行符并刷新 ostream | 缓冲区
ws	| 跳过空白字符（用于输入）
下面本关主要介绍setbase(b)、setprecision(n)、setiosflags(long)和setw(n)算子，剩下的同学们可以自己尝试。

##### 控制进制基数
对于标准输出流 cout 可以使用 setbase 来设置输出整数的进制基数（只支持88、1010、1616进制），如：


```
// 以八进制形式输出整数 n
cout << setbase(8) << n << endl;
```

也可以直接使用流操纵算子 oct（八进制）、hex（十六进制）和 dec（十进制）直接控制输出整数的进制，如：


```
// 以十六进制输出整数 n
cout << hex << n << endl;
```

###### 设置浮点数输出精度
流操纵算子 setprecision 或函数 precision 都可以设置浮点数输出的精度，其参数为输出浮点数的有效数字个数（包括整数部分和小数部分，如12.3412.34的有效数字个数为44）。

例如按55位有效位输出12.3 * 3.578的值：


```
cout << setprecision(5) << 12.3 * 3.578 << endl;
```

或者：


```
cout.precision(5);
cout << 12.3 * 3.578 << endl;
```

以上输出结果均为：44.009

###### 设置辅助格式
流操纵算子 setiosflags 可以辅助设置流输入输出格式，其参数是该流的格式标志值，setiosflags 提供了不同的参数来支持不同的输入输出格式需求。

setiosflags 的格式标志值如下表格：

标志值 |	含义
----------------------|---
ios::skipws	|在输入中跳过空白
ios::left	|左对齐，用填充字符填充右边。
ios::right	|右对齐，用填充字符填充左边(缺省对齐方式)。
ios::dec	|以基 10（十进制）格式化数值（缺省进制）
ios::oct	|以基 8（八进制）格式化数值
ios::hex	|以基 16（十六进制）格式化数值
ios::showbase|	以 C++ 编译器能读的格式显示数值常量
ios::showpoint|	按精度把后面的空白补 0 输出
ios::uppercase|	对于十六进制数值显示大写字母 A 到 F，对于科学格式显示大写字母 E。
ios::showpos|	对于正数显示正号（+）
ios::scientific|	以科学格式显示浮点数值
ios::fixed|	以定点格式显示浮点数值
例如：

```
1. double x = 1.23;
2. cout << setprecision(5) << x << endl;
3. cout << setiosflags(ios::showpoint) << setprecision(5) << x << endl;
```

输出结果为：


```
1. 1.23
2. 1.2300
```

###### 域宽
对于域宽，函数 width 和流操纵算子 setw 都可以实现对当前域宽（即输入输出的字符数）的设置。

- 如果输出的数据所需的宽度比设置的域宽小，空位用填充字符（默认为空格）填充；

- 如果被显示的数据所需的宽度比设置的域宽大，系统会自动突破宽度限制，输出所有位。

例如：


```
cin >> n;
cout << setw(6) << n << endl;     // 以域宽输出 n，如果 n 不足位，前面补空格
```
