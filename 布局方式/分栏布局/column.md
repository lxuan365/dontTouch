# 分栏布局
使用column属性可以实现分栏

> 带🍃的是缩写，带🚩的是重点
- column-rule;
- column-rule-color;
- column-rule-style;
- column-rule-width;
- column-span;
- column-fill;

### 🍃🚩columns
`columns`是`column-width`和`column-count`的缩写，顺序随意。表示列的宽度和数量。

`column-width`和`column-count`分别表示**理想的**宽度和数量，最终盒子被分成几列是这样算的：**min(盒子宽度/column-width, column-count)**。

### 🚩column-gap
`column-gap`表示列间隙的大小，值可以是关键字，长度值，百分比。也可以使用`gap`，是同样的效果。如果间隙足够大，会影响最终分栏数量。

### 🍃column-rule
column-rule
