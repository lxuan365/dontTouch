# 分栏布局
使用column属性可以实现分栏

> 带🍃的是缩写，带🚩的是重点

### 🍃🚩columns
`columns`是`column-width`和`column-count`的缩写，顺序随意。表示列的宽度和数量。

`column-width`和`column-count`分别表示**理想的**宽度和数量，最终盒子被分成几列是这样算的：**min(盒子宽度/column-width, column-count)**。

### 🚩column-gap
`column-gap`表示列间隙的大小，值可以是关键字，长度值，百分比。也可以使用`gap`，是同样的效果。如果间隙足够大，会影响最终分栏数量。

### 🍃column-rule
`column-rule`是`column-rule-width`，`column-rule-style`，`column-rule-color`的缩写，用来设置间隔线样式，用法和`border`类似。

### column-span
可以让一列垮多行，值可以是**none**不垮行，**all**垮多行。

### column-fill
控制内容如何分割，默认值是**balance**， 尽可能让列之间的内容平衡，这里是让最后一个内容是平衡的，比如最后一个`<p>`；可以是**auto**，内容按顺序填充；**balance-all**让所有内容平衡，现在没有浏览器支持。
