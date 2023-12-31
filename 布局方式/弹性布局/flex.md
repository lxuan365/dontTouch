# 弹性布局
1. item会块状化，这也是vertical-align不会生效的原因。
2. item浮动会失效。
3. 即使item没有设置position，也可以使用z-index属性。item如果设置了绝对定位，会脱离flex盒子控制。
4. item的margin不会合并，与普通块元素不同。
5. item尺寸存在内部计算规则（比较复杂），可以使用`margin: auto`单独控制。

## 方向flex-direction: row | row-reverse | column | column-reverse

## 换行flex-wrap: nowrap | wrap | wrap-reverse
1. nowrap：不换行，可能会发生宽度溢出。
2. wrap：换行。
3. wrap-reverse：换行，方向相反。

## 流体特性flex-flow: <flex-direction> | <flex-wrap>
> flex-flow是flex-direction与flex-wrap的缩写。

## 水平对齐justify-content: normal | flex-start | flex-end | center | space-between | space-around | space-evenly
1. 初始值：normal，根据场景不同，对应的值不同，在flex中，值类似于flex-start。
2. 默认值：flex-start，布局左对齐。
3. flex-end：右对齐。
4. center：居中对齐。
5. space-between：两端对齐。
6. space-around：item两侧空白相等（两个item中间会出现双倍间隙）。
7. space-evenly：item两侧空白完全相等。

## 所有子项垂直对齐align-items: stretch | flex-start | flex-end | center | baseline
## 单独子项垂直对齐align-self: auto | stretch | flex-start | flex-end | center | baseline
> align-self: auto(默认值)，表示align-self的对齐方式由align-items值决定。
> align-items的初始值实际是normal，但与stretch表现相同。
1. stretch：默认值，子项在容器的垂直方向上拉伸至容器高度，优先级小于height。
2. flex-start：顶部对齐。
3. flex-end：底部对齐。
4. center：居中对齐。
5. baseline：参与基线对齐，如果没有基线，则沿着边缘盒子线对齐。

## 垂直对齐（将所有子项看做一个整体）align-content: stretch | flex-start | flex-end | center | space-between | space-around | space-evenly

## 控制子项顺序order: <integer>
> 作用在子项上，默认值是0，负数在前。

## 弹性flex: <flex-grow> <flex-shrink> <flex-basis>
> 默认值：0 1 auto
### flex-grow空间仍有富裕的时候如何分配
1. flex-grow: <number> 
> 可以是小数，默认是0
### flex-shrink空间不足的时候如何分配
1. flex-shrink: <number> 
> 可以是小数，默认是1
### flex-basis分配基础数量
1. flex-basis: <length> | auto
> 默认是auto

>tips: `flex: 0(争) 2(让) 100px(基础)`,基础是100px，不会争多余的，不够了还会分出两份。

## 一堆单值
1. flex: inital == flex: 0 1 auto; (初始值，常用)
2. flex: 0 == flex: 0 1 0%; (使用少)
3. flex: none == flex: 0 0 auto; (推荐)
4. flex: 1 == flex: 1 1 0%; (推荐)
5. flex: auto == flex: 1 1 auto; (使用少，但有用)