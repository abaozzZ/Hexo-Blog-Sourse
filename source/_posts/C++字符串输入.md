---
title: C++字符串输入
date: 2020/4/14
tags: 
- C++
categories: C++学习

---

C++字符串输入

<!-- more -->

#### cin>>

对于cin,从缓冲区取数据。接受一个数字，字符串，遇“空格”、“TAB”、“回车”都结束，然后把它丢弃。后面的cin>>继续读取“空格”、“TAB”、“回车”后面的字符。

<!-- more -->

#### get()函数

```
char a[100],b[10],t;
    cin.get(a,100);
    cin.get(b,10);
    cout<<"a="<<a;
    cout<<" b="<<b;
    cin.get(c);//输入一个字符。
```
get()函数可以输入空格符，以Enter键结束，但不丢弃该字符。
由于第一次调用后，换行符将留在输入队列中，因此第二次调用时看到的第一个字符便是换行符，因此第二个get函数认为已到达行尾，而没有发现任何可读取的内容，即数组b值为空。
解决方法是借助get(),无参数的函数。其功能是读取下一个字符。


```
cin.get(a,size1);
cin.get();
cin.get(b,size2);
```

#### gets()函数

```
char a[100],b[10],t;
    gets(a); 
    gets(b);
    cout<<"a="<<a;
    cout<<" b="<<b;
```
gets()函数可以输入多行字符串，直到输入回车键截止，在存储字符串时，他用空值字符(‘\0’) 来替换换行符。但是在vs2010中，提示gets()函数unsafe，Consider using gets_s instead。gets_s()函数只能输入标准输入流中的一行字符串。


```
cin.getline()
    char a[1000],b[100],t;
 //   gets(a); 
    //gets(b);
    cin.getline(a,1000); 
    cin.getline(b,100);
    cout<<"a="<<a;
    cout<<" b="<<b;
```
接受一个字符串，可以接收空格并输出。可以输入多行字符。
cin.getline()实际上有三个参数，cin.getline(接受字符串的储存空间,接受个数,结束字符)




#### getline()
```
getline()
    string a,b;
    getline(cin,a,'\n'); 
    getline(cin,b);
    cout<<"a="<<a;
    cout<<" b="<<b;
```
接受一个字符串，可以接收空格并输出，需包含#include<string>
可以读入多行字符。
和cin.getline()类似，但是cin.getline()属于istream流，而getline()属于string流，是不一样的两个函数。
