# 尺寸
1. fit-content：紧身裤，包裹性，元素尺寸就是内容尺寸。
> 使用该属性的元素宽度确定，可以配合margin：auto实现居中。
2. fill-avaliable/avaliable/stretch：让元素尺寸填满可用空间（父元素）。stretch是最新标准。
3. min-content：首选最小宽度。
4. max-content：最大内容宽度，让元素尽可能大，哪怕溢出。比如，让图文显示在一行。

# 逻辑属性
1. start/end（水平方向）
2. inline/block（竖直方向）

> margin-【inline】-【end】: 5px;
永远在文档流结束的位置有5px，需要配合`writing-mode`，`direction`等方向属性一起使用才有意义，要不然直接使用`margin-right`就行。
> inline-size/block-size分别对应width/height，对min-width等，margin，padding，border等也适用。
> 在使用绝对定位或固定定位时，可以使用`inset:0`代替`top:0; right:0; bottom:0; left: 0;`。**逻辑属性中最实用的。**

# position定位
1. position: sticky; 一般是这样用。与固定定位无关，与相对定位相似，滚动时保留原来位置。相对计算元素是最近可滚动元素，如果没有，则相对浏览器视窗。
```js
  .box {
    position: sticky;
    top: 0
  }
```

# 字体
## font-famliy
1. system-ui：字体随系统字体变动，但最好别单独使用，要加上兜底字体：`body { font-family: system-ui,               -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif; }`（其中不包含emoji字体）。
2. emoji：虽然浏览器内置支持emoji字体，但可能会显示无颜色，要加上emoji字体`font-family: Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol, Noto Color Emoji;`。

> 使用emoji字体后可能会影响文本字体，可以把文本字体设置在emoji字体后覆盖掉。

3. 数学表达式： 用于展示数学公式，`<math>`背后用的就是Math字体。
4. 仿宋：一般不常用，可用于正式公告。

## @font-face
1. local()
2. unicode-ranage,决定字体用在哪些字符上。
3. woff/woff2
4. font-display：可以控制字体加载和文本渲染之间的关系。

## 换行
1. word-break属性（cjk）
2. hyphens属性（英文），一般不常用，在中文网站中会出问题。
3. <wbr>（中文），&shy（英文）
