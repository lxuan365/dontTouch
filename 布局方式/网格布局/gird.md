# 网格布局
## template-column-rows, template-column-column: 指定行和列的数量和大小。
> template-column-rows: 10px 20px auto; 表示有三行，大小分别是10px，20px，auto。
> 支持的值：长度，百分比，关键字（min-content，max-content，auto），fr，函数值（repeat(),minmax(),fit-content()）。
> template-column-rows: [liuxuan] 10px [zjy] 20px [pig] auto [sealos]; 给网格线命名。

## gird-template, gird: <template-column-rows> / <template-column-column>
> gird: 10px 20px auto / 50px 30px
> 也可以是template-column-rows，template-column-column，gird-template-ares的缩写：
  gird-template: 'apple apple apple' 1fr
                 'apple apple apple' 1fr
                 / 1fr 1fr 1fr

## gird-template-ares: 'apple apple apple'
                       'apple apple apple'
> 需要配合子项gird-area使用，只能是矩形，不是是L型或凹凸型。

## gird-auto-columns, gird-auto-rows: 指定隐士网格大小
## gird-auto-flow: row | column | dense | row dense | column dense
> 相当于flex中的flex-direction
## gird: grid-template- rows、grid-template-columns、grid-template-areas、grid-auto-rows、grid- auto-columns和grid-auto-flow的缩写
## gap: <row-gap> | <column-gap>
## 子项水平对齐justify-items: stretch | start | center | end
## 子项竖直对齐align-items: normal | stretch | start | center | end | baseline
## 缩写place-item: <align-items> <justify-items>
## 整体水平对齐justify-content: normal | stretch | start | end | center | space-between | space-around | space-evenly
## 整体垂直对齐align-content: normal | stretch | start | end | center | space-between | space-around | space-evenly
## 缩写place-content: <align-content> | <justify-content>
## 区间范围设置属性grid-column-start/grid-column-end,grid-row-start/ grid-row-end
## 缩写gird-colnum: <grid-column-start> <grid-column-end> 
## 缩写gird-row: <grid-row-start> <grid-row-end> 
## 外加区域范围设置gird-area
## 子项水平对齐justify-self: auto | normal | stretch | start | end | center | baseline
## 子项垂直对齐align-self: auto | normal | stretch | start | end | center | baseline
## 缩写place-self: <justify-self> <align-self>