---
title: span标签
date: 2020/4/14
tags: 
- 前端学习
categories: 前端学习
---
span标签

<!-- more -->

例子

```
<p><span>some text.</span>some other text.</p>
```
例子解释
如果不对 span 应用样式，那么 span 元素中的文本与其他文本不会任何视觉上的差异。尽管如此，上例中的 span 元素仍然为 p 元素增加了额外的结构。

可以为 span 应用 id 或 class 属性，这样既可以增加适当的语义，又便于对 span 应用样式。

可以对同一个 <span> 元素应用 class 或 id 属性，但是更常见的情况是只应用其中一种。这两者的主要差异是，class 用于元素组（类似的元素，或者可以理解为某一类元素），而 id 用于标识单独的唯一的元素。

**提示**：事实上，您也许已经注意到了，W3School 站点上有一些文本的样式与其他文本是不同的。比如“提示”使用了粗体的橘红色。尽管实现这种效果的方法非常多，但是我们的做法是：使用“提示”使用 span 元素，然后对这个 span 元素的父元素，即 p 元素应用 class，这样就可以对这个类的子元素 span 应用相应的样式了。

HTML:
```
<p class="tip"><span>提示：</span>... ... ...</p>
```
CSS:
```
p.tip span {
	font-weight:bold;
	color:#ff9955;
	}
```
