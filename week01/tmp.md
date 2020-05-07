## ★More

1）在w3c标准里边，像REC这样的东西到底表示的是什么？

![标准的诞生历程](assets/img/2020-05-06-23-26-10.png)

➹：[W3C标准流程与组织架构 - 知乎](https://zhuanlan.zhihu.com/p/36103933)

2）色域标准？

为啥会有那么多色域标准？

人眼可见的色彩包含数百万种颜色，但扫描仪、显示器和彩色打印机等显色设备只能产生（重现）其中的一部分颜色（色彩子集），这个"子集"称为色域。因此，人们为不同的领域制定了不同的色域标准。

> 人看到的颜色种数 vs 显色设备能显示的颜色种数 -> 前者是爸爸，后者是弟弟……

有哪些色域标准？

![色域分类](assets/img/2020-05-06-23-39-37.png)

sRGB -> 这种标准得到了W3C的支持 -> 用于互联网

> 色域并不一定是谁比谁更好，它们都有其特定的专精用途。近年来，随着广色域的普及，我们可以期待显色设备给我们带来更出色的色彩表现。

➹：[浅谈几种常见的色域标准 - 知乎](https://zhuanlan.zhihu.com/p/45533004)

3）HTML5已经退休了？

![HTML5](assets/img/2020-05-06-23-58-59.png)

目前看的HTML版本：

![HTML5.2](assets/img/2020-05-07-00-00-42.png)

➹：[[译]HTML 5.2新特性 - 知乎](https://zhuanlan.zhihu.com/p/33174266)

4）我们可以去阅读的CSS版本？

![css2.1](assets/img/2020-05-07-00-16-31.png)

> 语法写的标准

➹：[Grammar of CSS 2.1](https://www.w3.org/TR/2011/REC-CSS2-20110607/grammar.html#grammar)

5）CSS有多少种属性？有多少种值？

6）CSS标准总览？

➹：[All CSS specifications](https://www.w3.org/Style/CSS/specs.en.html)

7）一些讲CSS的文档？

➹：[CSS - Syntax - Tutorialspoint](https://www.tutorialspoint.com/css/css_syntax.htm)

8）`@charset`和`@import`在CSS里边是如何写的？

``` css
@charset "utf-8";
@import 'custom.css';
```

形式语法（Formal syntax）：

``` css
@charset "<charset>";
@import [ <string> | <url> ] [ <media-query-list> ]?;
```

➹：[@charset - CSS: Cascading Style Sheets - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/@charset)

➹：[@import - CSS: Cascading Style Sheets - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/@import)

9）`@media`和`@page`都是些什么东西？

media types 是样式表最重要的特性之一 -> 它们规定了文档如何在不同的媒体上呈现: 屏幕上、纸上、语音合成器、盲文设备等等

某些 CSS 属性仅适用于某些媒体，但是，有时不同媒体类型的样式表可能会共享一个CSS属性，不过，这通常都得要求该属性具有不同的值，如 `font-size`这个属性，对 `screen` 和 `print`这两类媒体都很有用，由于这两种媒体类型差别很大，因此，我们需要为这共同属性设置不同的值; document在计算机屏幕上通常需要比在纸上使用更大的字体，所以，有必要直接让样式表或样式表的一部分适用于某些媒体类型

例子：

``` css
@import url("fancyfonts.css") screen;
@media print {
  /* style sheet for print goes here */
}

@media print {
  body { font-size: 10pt }
}
@media screen {
  body { font-size: 13px }
}
@media screen, print {
  body { line-height: 1.2 }
}
```

> 媒体类型名称不区分大小写。CSS 2.1是没有媒体查询这个概念的……

CSS 2时代的媒体查询 vs CSS 3时代的：

看完之前的笔记：[第1章 前期准备 - imooc](https://ppambler.github.io/imooc/01-%E6%89%80%E5%90%91%E6%8A%AB%E9%9D%A1%E7%9A%84%E5%93%8D%E5%BA%94%E5%BC%8F%E5%BC%80%E5%8F%91/%E7%AC%AC1%E7%AB%A0-%E5%89%8D%E6%9C%9F%E5%87%86%E5%A4%87.html#1-6-%E5%AA%92%E4%BD%93%E6%9F%A5%E8%AF%A2-1)

> 以前写这个笔记的时候，没有感受到为啥老师要对比一下CSS2.1，现在看来，这老师是真得牛逼！

那么 `@page`呢？

`@page` 规则用于在打印文档时修改某些CSS属性。你不能用`@page`规则来修改所有的CSS属性，而是只能修改「页边距（margins）」、「orphans」、「widows」、「分页符（page breaks）」这4个属性。除了这4个属性以外，你对其它的CSS属性的修改是无效的

例子：

``` css
@page {
  margin: 1cm;
}

@page :first {
  margin: 2cm;
}
```

➹：[Media types](https://www.w3.org/TR/2011/REC-CSS2-20110607/media.html#q7.0)

➹：[Media Queries](https://www.w3.org/TR/2012/REC-css3-mediaqueries-20120619/)

➹：[@media - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/@media)

➹：[深入理解CSS Media媒体查询 - 小火柴的蓝色理想 - 博客园](https://www.cnblogs.com/xiaohuochai/p/5848612.html)

➹：[CSS媒体查询 - 掘金](https://juejin.im/post/5affd7ff6fb9a07aa2139ebb)

➹：[@page - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/@page)

➹：[CSS 打印 - 龙墨 - SegmentFault 思否](https://segmentfault.com/a/1190000010145260)












