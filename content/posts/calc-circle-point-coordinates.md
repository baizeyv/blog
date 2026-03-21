+++
date = '2026-03-21T17:11:28+08:00'
draft = false
title = 'Calc Circle Point Coordinates'
tags: ["calc", "coordinates"]
image: "/images/testpic.png"
+++

# 求圆上点的坐标

圆点坐标：(x0,y0)
半径：r
角度：a0

则圆上任一点为：（x1,y1）

`x1 = x0 + r _ cos(ao _ 3.14 /180 )`
`y1 = y0 + r _ sin(ao _ 3.14 /180 )`

求圆上点的坐标需要已知的条件：圆心、半径、角度

假设圆心: `O (x0,y0)`

半径: `r`

角度: `angle` (角度是相对于 (→) 位置而言，逆时针为负数，顺时针为正)

计算公式：

`p2 (x1,y1)`, 其中 `angle = 30`

```cs
x1 = x0 + r _ cos(angle _ PI / 180)

y1 = y0 + r _ sin(angle _ PI /180)
```
