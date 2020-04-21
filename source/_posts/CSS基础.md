---
title: CSS基础
date: 2020/4/14
tags: 
- CSS样式
- 前端学习
categories: 前端学习C
---
CSS样式基础

<!-- more -->

# 2020-4-4

## 字体粗细 font-weight

我们使用font-weight属性设置文本的粗细。印刷世界中，根据内容的需要会设置不同的字体粗细，同样的在网页中也要更具内容设置。



font-weight设置的数值在100~900之间，分为9级加粗度。有些字体会内置加粗的级别。例如100 对应最细的字体，900 对应最粗的字体； 400对应normal·，而 700 则等价于 bold。


## 文本装饰 text-decoration
我们使用text-decoration设置字体上的文本装饰。

其可用值有：

- none: 取消已经存在的任何文本装饰；

- underline: 文本下划线；

- overline: 文本上划线；

- line-through: 贯穿文本的线；

- blink：闪烁文本。

使用时，可以根据需求，同时添加多个装饰值。
例如：

```
<!DOCTYPE html>
<html lang="zh">
<head>
  <meta charset="UTF-8">
  <title>文本装饰</title>
  <style type="text/css">
    a {
      text-decoration: none;
    }
    p {
      text-orientation: line-through;
      color: gray;
    }
  </style>
</head>
<body>
  <p>你好，欢迎学习educoder平台的<a href="#">CSS实训课程</a>。</p>
</body>
</html>
```
使用此方法在设置链接时可以设置取消链接上的默认下划线。显示效果如下：  
![image](A50AA4E1BB0B40E18AFCF7C4694FE927)
## 文本布局
接下来，我们来看用来影响文本布局的属性。

文本对齐 text-align
我们使用text-align来改变一个元素中的文本行互相之间的对齐方式。

其可用值有：

- left: 左对齐文本；

- right: 右对齐文本；

- center: 居中文字；

- justify: 水平对齐，改变单词之间的差距，使所有文本行的宽度相同。

不同的语言中默认的对齐方式不同，大部分西方语言都是从左向右读，text-align 的默认值是 left。而对于希伯来语和阿拉伯语之类的的语言，阅读时从右向左读，text-align 则默认为 right。

例如：
```
<!DOCTYPE html>
<html lang="zh">
<head>
<head>
    <meta charset="UTF-8">
    <title>CSS text-align</title>
    <style>
        h1 {
            text-align: center;
        }
        p.from {
            text-align: right;
        }
        p.main {
            text-align: justify;
        }
    </style>
</head>
<body>
    <h1>端午节</h1>
    <p class="from"><a href="https://zh.wikipedia.org/zh-sg/端午节">维基百科</a></p>
    <p class="main">端午节是东亚文化圈的重要传统节日，定在每年农历五月初五，别称端阳节、端日节、午日节、粽子节、天中节、五月节、五日节、艾节、端五、重午、重五、午日、夏节、菖蒲节，本来是夏季的一个送离五瘟神，驱除瘟疫的节日。后来楚国的爱国诗人屈原于端午节投江自尽，后在中国演化为端午节，以纪念屈原，有人称其为诗人节（有些地方是纪念吴国忠臣伍子胥的忌日），是华人四大节日之一，与新年、中秋等节日同属东亚文化圈的中国大陆、香港、澳门、台湾、琉球、日本、朝鲜半岛、越南的重要传统节日。</p>
    <p>
        <b>注意：</b> 重置浏览器窗口大小可查看 &quot;justify&quot; 的实际效果。</p>
</body>
</html>
```
显示效果如图：  
![image](1104AFE039C64799B0B0AF2044297A85)


## 行高 line-height
我们使用line-height 属性来设置行高。

注意：行高属性值不能为负。

其可用值有：

- normal：默认。设置合理的行间距；

- number：设置数字，此数字会与当前的字体尺寸相乘来设置行间距；

- length：设置固定的行间距；

- %：基于当前字体尺寸的百分比行间距；

- inherit：从父元素继承 line-height 属性的值。

例如：
```
<html>
<head>
    <style type="text/css">
        p.small {
            line-height: 90%
        }
        p.big {
            line-height: 200%
        }
    </style>
</head>
<body>
    <p>
        标准行高的段落。 在大多数浏览器中默认行高大约是 110% 到 120%。 标准行高的段落。 标准行高的段落。 标准行高的段落。 标准行高的段落。 标准行高的段落。
    </p>
    <p class="small">
        本段落拥有更小的行高。 本段落拥有更小的行高。 本段落拥有更小的行高。 本段落拥有更小的行高。 本段落拥有更小的行高。 本段落拥有更小的行高。 本段落拥有更小的行高。
    </p>
    <p class="big">
        本段落拥有更大的行高。 本段落拥有更大的行高。 本段落拥有更大的行高。 本段落拥有更大的行高。 本段落拥有更大的行高。 本段落拥有更大的行高。 本段落拥有更大的行高。
    </p>
</body>
</html>
```
显示效果如下：  
![image](9FC5171F582C4344A88DB0B3CE78EC45)



本实例中使用百分比设置行高，同样的，我们有可以使用像素值设置行高：

 p.small {
    line-height: 10px
}
p.big {
    line-height: 30px
}
或者使用数字：

p.small {
    line-height: 0.5
}
p.big {
    line-height: 2
}
## 字符间距和字间距 letter-spacing word-spacing
letter-spacing 属性用于控制字符间的间隔多少；

其可用值有：

- normal：默认值，字符间没有额外的间隔；

- length：定义字符间的固定间隔（可以为负值）；

- inherit：从父元素继承 letter-spacing 属性的值。

同样的，word-spacing 属性用于控制字与字的间隔多少。

其可用值有：

- normal：默认；

- length：定义字之间的固定间隔；

- inherit：从父元素继承 word-spacing 属性的值。

举例如下：
```
<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <title>letter & word spacing</title>
    <style>
        h1 {
            letter-spacing: 2px;
        }
        h2 {
            letter-spacing: -3px;
        }
        p {
            word-spacing: 30px;
        }
    </style>
</head>
<body>
    <h1> 这是标题一 This is heading 1</h1>
    <h2> 这是标题二 This is heading 2</h2>
    <p>这是一些文本。This is some text.</p>
</body>
</html>
```
显示效果如下：  
![image](437909E136724942A021F7F4DB1659C5)
# 2020-4-5
## 层叠次序
当同一个 HTML 元素被不止一个样式定义时，会使用哪个样式呢？

一般而言，所有的样式会根据下面的规则层叠于一个新的虚拟样式表中，其中数字 4 拥有最高的优先权。

1. 浏览器缺省设置
1. 外部样式表
1. 内部样式表（位于 <head> 标签内部）
1. 内联样式（在 HTML 元素内部）
因此，内联样式（在 HTML 元素内部）拥有最高的优先权，这意味着它将优先于以下的样式声明：<head> 标签中的样式声明，外部样式表中的样式声明，或者浏览器中的样式声明（缺省值）。
## CSS语法
CSS 规则由两个主要的部分构成：选择器，以及一条或多条声明。
![image](E76DF57BD91C4A5DB7B3FD559E5F3764)
`p { color: #ff0000; }`
### 记得写引号
提示：如果值为若干单词，则要给值加引号：
```
p {font-family: "sans serif";}
```
### 多重声明：
**==提示==**：如果要定义不止一个声明，则需要用分号将每个声明分开。下面的例子展示出如何定义一个红色文字的居中段落。最后一条规则是不需要加分号的，因为分号在英语中是一个分隔符号，不是结束符号。然而，大多数有经验的设计师会在每条声明的末尾都加上分号，这么做的好处是，当你从现有的规则中增减声明时，会尽可能地减少出错的可能性。就像这样：
`p {text-align:center; color:red;}`  
你应该在每行只描述一个属性，这样可以增强样式定义的可读性，就像这样：
```
p {
  text-align: center;
  color: black;
  font-family: arial;
}
```
### 空格和大小写
大多数样式表包含不止一条规则，而大多数规则包含不止一个声明。多重声明和空格的使用使得样式表更容易被编辑：
```
body {
  color: #000;
  background: #fff;
  margin: 0;
  padding: 0;
  font-family: Georgia, Palatino, serif;
  }
```
## CSS高级语法
### 选择器的分组
你可以对选择器进行分组，这样，被分组的选择器就可以分享相同的声明。用逗号将需要分组的选择器分开。在下面的例子中，我们对所有的标题元素进行了分组。所有的标题元素都是绿色的。
```
h1,h2,h3,h4,h5,h6 {
  color: green;
  }
```
### 继承及其问题
根据 CSS，子元素从父元素继承属性。但是它并不总是按此方式工作。看看下面这条规则：
```
body {
     font-family: Verdana, sans-serif;
     }
```
根据上面这条规则，站点的 body 元素将使用 Verdana 字体（假如访问者的系统中存在该字体的话）。

通过 CSS 继承，子元素将继承最高级元素（在本例中是 body）所拥有的属性（这些子元素诸如 p, td, ul, ol, ul, li, dl, dt,和 dd）。不需要另外的规则，所有 body 的子元素都应该显示 Verdana 字体，子元素的子元素也一样。并且在大部分的现代浏览器中，也确实是这样的。
### CSS派生选择器
通过依据元素在其位置的上下文关系来定义样式，你可以使标记更加简洁。

在 CSS1 中，通过这种方式来应用规则的选择器被称为上下文选择器 (contextual selectors)，这是由于它们依赖于上下文关系来应用或者避免某项规则。在 CSS2 中，它们称为派生选择器，但是无论你如何称呼它们，它们的作用都是相同的。

派生选择器允许你根据文档的上下文关系来确定某个标签的样式。通过合理地使用派生选择器，我们可以使 HTML 代码变得更加整洁。

比方说，你希望列表中的 strong 元素变为斜体字，而不是通常的粗体字，可以这样定义一个派生选择器：
```
li strong {
    font-style: italic;
    font-weight: normal;
  }
```
请注意标记为\<strong\> 的蓝色代码的上下文关系：
```
<p><strong>我是粗体字，不是斜体字，因为我不在列表当中，所以这个规则对我不起作用</strong></p>

<ol>
<li><strong>我是斜体字。这是因为 strong 元素位于 li 元素内。</strong></li>
<li>我是正常的字体。</li>
</ol>
```
在上面的例子中，只有 li 元素中的 strong 元素的样式为斜体字，无需为 strong 元素定义特别的 class 或 id，代码更加简洁。
再看看下面的 CSS 规则：
```
strong {
     color: red;
     }

h2 {
     color: red;
     }

h2 strong {
     color: blue;
     }
```
下面是它施加影响的 HTML：
```
<p>The strongly emphasized word in this paragraph is<strong>red</strong>.</p>
<h2>This subhead is also red.</h2>
<h2>The strongly emphasized word in this subhead is<strong>blue</strong>.</h2>
```
### id 选择器
id 选择器可以为标有特定 id 的 HTML 元素指定特定的样式。

id 选择器以 "#" 来定义。

下面的两个 id 选择器，第一个可以定义元素的颜色为红色，第二个定义元素的颜色为绿色：
```
#red {color:red;}
#green {color:green;}
```
下面的 HTML 代码中，id 属性为 red 的 p 元素显示为红色，而 id 属性为 green 的 p 元素显示为绿色。
```
<p id="red">这个段落是红色。</p>
<p id="green">这个段落是绿色。</p>
```
**注意**：id 属性只能在每个 HTML 文档中出现一次。  
#### id 选择器和派生选择器
在现代布局中，id 选择器常常用于建立派生选择器。
```
#sidebar p {
	font-style: italic;
	text-align: right;
	margin-top: 0.5em;
	}
```
上面的样式只会应用于出现在 id 是 sidebar 的元素内的段落。这个元素很可能是 div 或者是表格单元，尽管它也可能是一个表格或者其他块级元素。
#### 一个选择器，多种用法
**即使被标注为 sidebar 的元素只能在文档中出现一次，这个 id 选择器作为派生选择器也可以被使用很多次**：
```
#sidebar p {
	font-style: italic;
	text-align: right;
	margin-top: 0.5em;
	}

#sidebar h2 {
	font-size: 1em;
	font-weight: normal;
	font-style: italic;
	margin: 0;
	line-height: 1.5;
	text-align: right;
	}
```
在这里，与页面中的其他 p 元素明显不同的是，sidebar 内的 p 元素得到了特殊的处理，同时，与页面中其他所有 h2 元素明显不同的是，sidebar 中的 h2 元素也得到了不同的特殊处理。
### 类选择器
**在 CSS 中，类选择器以一个点号显示**：  
```
.center {text-align: center}
```
在上面的例子中，所有拥有 center 类的 HTML 元素均为居中。

在下面的 HTML 代码中，h1 和 p 元素都有 center 类。这意味着两者都将遵守 ".center" 选择器中的规则。
```
<h1 class="center">
This heading will be center-aligned
</h1>

<p class="center">
This paragraph will also be center-aligned.
</p>
```
**注意**：类名的第一个字符不能使用数字！它无法在 Mozilla 或 Firefox 中起作用。

和 id 一样，class 也可被用作派生选择器：
```
.fancy td {
	color: #f60;
	background: #666;
	}
```
在上面这个例子中，类名为 fancy 的更大的元素内部的表格单元都会以灰色背景显示橙色文字。（名为 fancy 的更大的元素可能是一个表格或者一个 div）

元素也可以基于它们的类而被选择：
```
td.fancy {
	color: #f60;
	background: #666;
	}
```
在上面的例子中，类名为 fancy 的表格单元将是带有灰色背景的橙色。
```
<td class="fancy">
```
你可以将类 fancy 分配给任何一个表格元素任意多的次数。那些以 fancy 标注的单元格都会是带有灰色背景的橙色。那些没有被分配名为 fancy 的类的单元格不会受这条规则的影响。还有一点值得注意，class 为 fancy 的段落也不会是带有灰色背景的橙色，当然，任何其他被标注为 fancy 的元素也不会受这条规则的影响。这都是由于我们书写这条规则的方式，这个效果被限制于被标注为 fancy 的表格单元（即使用 td 元素来选择 fancy 类）。
### 属性选择器
```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html>
<head>
<style type="text/css">
[title]
{
color:red;
}
</style>
</head>

<body>
<h1>可以应用样式：</h1>
<h2 title="Hello world">Hello world</h2>
<a title="W3School" href="http://w3school.com.cn">W3School</a>

<hr />

<h1>无法应用样式：</h1>
<h2>Hello world</h2>
<a href="http://w3school.com.cn">W3School</a>
</body>
</html>

```
### 如何创建 CSS
如何插入样式表
当读到一个样式表时，浏览器会根据它来格式化 HTML 文档。插入样式表的方法有三种：

#### 外部样式表
当样式需要应用于很多页面时，外部样式表将是理想的选择。在使用外部样式表的情况下，你可以通过改变一个文件来改变整个站点的外观。每个页面使用 <link> 标签链接到样式表。<link> 标签在（文档的）头部：
```
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css" />
</head>
```
浏览器会从文件 mystyle.css 中读到样式声明，并根据它来格式文档。

外部样式表可以在任何文本编辑器中进行编辑。文件不能包含任何的 html 标签。样式表应该以 .css 扩展名进行保存。下面是一个样式表文件的例子：
```
hr {color: sienna;}
p {margin-left: 20px;}
body {background-image: url("images/back40.gif");}
```
#### 多重样式
如果某些属性在不同的样式表中被同样的选择器定义，那么属性值将从更具体的样式表中被继承过来。

例如，外部样式表拥有针对 h3 选择器的三个属性：
```
h3 {
  color: red;
  text-align: left;
  font-size: 8pt;
  }
```
而内部样式表拥有针对 h3 选择器的两个属性：
```
h3 {
  text-align: right; 
  font-size: 20pt;
  }
```
假如拥有内部样式表的这个页面同时与外部样式表链接，那么 h3 得到的样式是：
```
color: red; 
text-align: right; 
font-size: 20pt;
```
即颜色属性将被继承于外部样式表，而文字排列（text-alignment）和字体尺寸（font-size）会被内部样式表中的规则取代。  
# 2020-4-8
## CSS背景
这条规则把元素的背景设置为灰色：
```
p {background-color: gray;}
```
要把图像放入背景，需要使用 background-image 属性。background-image 属性的默认值是 none，表示背景上没有放置任何图像。

如果需要设置一个背景图像，必须为这个属性设置一个 URL 值：
```
body {background-image: url(/i/eg_bg_04.gif);}
```
### 背景重复
如果需要在页面上对背景图像进行平铺，可以使用 background-repeat 属性。

属性值 repeat 导致图像在水平垂直方向上都平铺，就像以往背景图像的通常做法一样。repeat-x 和 repeat-y 分别导致图像只在水平或垂直方向上重复，no-repeat 则不允许图像在任何方向上平铺。

默认地，背景图像将从一个元素的左上角开始。请看下面的例子：
```
body
  { 
  background-image: url(/i/eg_bg_03.gif);
  background-repeat: repeat-y;
  }
```
### 背景定位
可以利用 background-position 属性改变图像在背景中的位置。

下面的例子在 body 元素中将一个背景图像居中放置：
```
body
  { 
    background-image:url('/i/eg_bg_03.gif');
    background-repeat:no-repeat;
    background-position:center;
  }
```
为 background-position 属性提供值有很多方法。首先，可以使用一些关键字：top、bottom、left、right 和 center。通常，这些关键字会成对出现，不过也不总是这样。还可以使用长度值，如 100px 或 5cm，最后也可以使用百分数值。不同类型的值对于背景图像的放置稍有差异。
### 关键字：
图像放置关键字最容易理解，其作用如其名称所表明的。例如，top right 使图像放置在元素内边距区的右上角。  
根据规范，位置关键字可以按任何顺序出现，只要保证不超过两个关键字 - 一个对应水平方向，另一个对应垂直方向。  
如果只出现一个关键字，则认为另一个关键字是 center。  
所以，如果希望每个段落的中部上方出现一个图像，只需声明如下：
```
p
  { 
    background-image:url('bgimg.gif');
    background-repeat:no-repeat;
    background-position:top;
  }
```
下面是等价的位置关键字：

单一关键字 | 等价的关键字
-----|-------
center |	center center
top |	top center 或 center top
bottom |	bottom center 或 center bottom
right |	right center 或 center right
left |	left center 或 center left
### 百分数值
百分数值的表现方式更为复杂。假设你希望用百分数值将图像在其元素中居中，这很容易：
```
body
  { 
    background-image:url('/i/eg_bg_03.gif');
    background-repeat:no-repeat;
    background-position:50% 50%;
  }
```
这会导致图像适当放置，其中心与其元素的中心对齐。换句话说，百分数值同时应用于元素和图像。也就是说，图像中描述为 50% 50% 的点（中心点）与元素中描述为 50% 50% 的点（中心点）对齐。

如果图像位于 0% 0%，其左上角将放在元素内边距区的左上角。如果图像位置是 100% 100%，会使图像的右下角放在右边距的右下角。

因此，如果你想把一个图像放在水平方向 2/3、垂直方向 1/3 处，可以这样声明：
```
body
  { 
    background-image:url('/i/eg_bg_03.gif');
    background-repeat:no-repeat;
    background-position:66% 33%;
  }
```
如果只提供一个百分数值，所提供的这个值将用作水平值，垂直值将假设为 50%。这一点与关键字类似。

background-position 的默认值是 0% 0%，在功能上相当于 top left。这就解释了背景图像为什么总是从元素内边距区的左上角开始平铺，除非您设置了不同的位置值。

### 长度值
长度值解释的是元素内边距区左上角的偏移。偏移点是图像的左上角。

比如，如果设置值为 50px 100px，图像的左上角将在元素内边距区左上角向右 50 像素、向下 100 像素的位置上：
```
body
  { 
    background-image:url('/i/eg_bg_03.gif');
    background-repeat:no-repeat;
    background-position:50px 100px;
  }
```
注意，这一点与百分数值不同，因为偏移只是从一个左上角到另一个左上角。也就是说，图像的左上角与 background-position 声明中的指定的点对齐。

### 背景关联
如果文档比较长，那么当文档向下滚动时，背景图像也会随之滚动。当文档滚动到超过图像的位置时，图像就会消失。

您可以通过 background-attachment 属性防止这种滚动。通过这个属性，可以声明图像相对于可视区是固定的（fixed），因此不会受到滚动的影响：
```
body 
  {
  background-image:url(/i/eg_bg_02.gif);
  background-repeat:no-repeat;
  background-attachment:fixed
  }
```
### CSS文本
CSS 文本属性可定义文本的外观。

通过文本属性，您可以改变文本的颜色、字符间距，对齐文本，装饰文本，对文本进行缩进，等等。

缩进文本
把 Web 页面上的段落的第一行缩进，这是一种最常用的文本格式化效果。

CSS 提供了 text-indent 属性，该属性可以方便地实现文本缩进。

通过使用 text-indent 属性，所有元素的第一行都可以缩进一个给定的长度，甚至该长度可以是负值。

这个属性最常见的用途是将段落的首行缩进，下面的规则会使所有段落的首行缩进 5 em：
```
p {text-indent: 5em;}
```
注意：一般来说，可以为所有块级元素应用 text-indent，但无法将该属性应用于行内元素，图像之类的替换元素上也无法应用 text-indent 属性。不过，如果一个块级元素（比如段落）的首行中有一个图像，它会随该行的其余文本移动。

提示：如果想把一个行内元素的第一行“缩进”，可以用左内边距或外边距创造这种效果。
### 水平对齐
text-align 是一个基本的属性，它会影响一个元素中的文本行互相之间的对齐方式。它的前 3 个值相当直接，不过第 4 个和第 5 个则略有些复杂。  
值 left、right 和 center 会导致元素中的文本分别左对齐、右对齐和居中。  
西方语言都是从左向右读，所有 text-align 的默认值是 left。文本在左边界对齐，右边界呈锯齿状（称为“从左到右”文本）。对于希伯来语和阿拉伯语之类的的语言，text-align 则默认为 right，因为这些语言从右向左读。不出所料，center 会使每个文本行在元素中居中。

提示：将块级元素或表元素居中，要通过在这些元素上适当地设置左、右外边距来实现。

**text-align:center 与 \<CENTER>**
您可能会认为 text-align:center 与 \<CENTER> 元素的作用一样，但实际上二者大不相同。

\<CENTER> 不仅影响文本，还会把整个元素居中。text-align 不会控制元素的对齐，而只影响内部内容。元素本身不会从一段移到另一端，只是其中的文本受影响。

justify
最后一个水平对齐属性是 justify。

在两端对齐文本中，文本行的左右两端都放在父元素的内边界上。然后，调整单词和字母间的间隔，使各行的长度恰好相等。您也许已经注意到了，两端对齐文本在打印领域很常见。
### 字符转换
text-transform 属性处理文本的大小写。这个属性有 4 个值：

- none
- uppercase 全大写
- lowercase 全小写
- capitalize  每个单词首字母大写
默认值 none 对文本不做任何改动，将使用源文档中的原有大小写。顾名思义，uppercase 和 lowercase 将文本转换为全大写和全小写字符。最后，capitalize 只对每个单词的首字母大写。

作为一个属性，text-transform 可能无关紧要，不过如果您突然决定把所有 h1 元素变为大写，这个属性就很有用。不必单独地修改所有 h1 元素的内容，只需使用 text-transform 为你完成这个修改：
```
h1 {text-transform: uppercase}
```
使用 text-transform 有两方面的好处。首先，只需写一个简单的规则来完成这个修改，而无需修改 h1 元素本身。其次，如果您以后决定将所有大小写再切换为原来的大小写，可以更容易地完成修改。
### 文本装饰
接下来，我们讨论 text-decoration 属性，这是一个很有意思的属性，它提供了很多非常有趣的行为。

text-decoration 有 5 个值：

- none 无下划线，可用于链接样式
- underline 加下划线
- overline 文本顶端加线
- line-through 文本中间加线
- blink   文本闪烁  

不出所料，underline 会对元素加下划线，就像 HTML 中的 U 元素一样。overline 的作用恰好相反，会在文本的顶端画一个上划线。值 line-through 则在文本中间画一个贯穿线，等价于 HTML 中的 S 和 strike 元素。blink 会让文本闪烁，类似于 Netscape 支持的颇招非议的 blink 标记。

none 值会关闭原本应用到一个元素上的所有装饰。通常，无装饰的文本是默认外观，但也不总是这样。例如，链接默认地会有下划线。如果您希望去掉超链接的下划线，可以使用以下 CSS 来做到这一点：

a {text-decoration: none;}
注意：如果显式地用这样一个规则去掉链接的下划线，那么锚与正常文本之间在视觉上的唯一差别就是颜色（至少默认是这样的，不过也不能完全保证其颜色肯定有区别）。

还可以在一个规则中结合多种装饰。如果希望所有超链接既有下划线，又有上划线，则规则如下：
```
a:link a:visited {text-decoration: underline overline;}
```
不过要注意的是，如果两个不同的装饰都与同一元素匹配，胜出规则的值会完全取代另一个值。请考虑以下的规则：
```
h2.stricken {text-decoration: line-through;}
h2 {text-decoration: underline overline;}
```
对于给定的规则，所有 class 为 stricken 的 h2 元素都只有一个贯穿线装饰，而没有下划线和上划线，因为 text-decoration 值会替换而不是累积起来。
### 处理空白符
white-space 属性会影响到用户代理对源文档中的空格、换行和 tab 字符的处理。

通过使用该属性，可以影响浏览器处理字之间和文本行之间的空白符的方式。从某种程度上讲，默认的 XHTML 处理已经完成了空白符处理：它会把所有空白符合并为一个空格。所以给定以下标记，它在 Web 浏览器中显示时，各个字之间只会显示一个空格，同时忽略元素中的换行：
```
<p>This     paragraph has    many
    spaces           in it.</p>
```

可以用以下声明显式地设置这种默认行为：
```
p {white-space: normal;}
```
上面的规则告诉浏览器按照平常的做法去处理：丢掉多余的空白符。如果给定这个值，换行字符（回车）会转换为空格，一行中多个空格的序列也会转换为一个空格。
**总结**
下面的表格总结了 white-space 属性的行为：

值 |	空白符 |	换行符 |	自动换行
---|---|---|---
pre-line |	合并 |	保留 |	允许
normal |	合并 |	忽略 | 	允许
nowrap	|合并	|忽略|	不允许
pre	|保留|	保留 |	不允许
pre-wrap |	保留 |	保留 |允许