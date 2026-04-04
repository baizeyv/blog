+++
date = '2026-04-04T13:34:53+08:00'
draft = false
title = 'Assign Js to Css'
tags = ['Javascript', 'Css']
+++

# JavaScript 变量赋值给 CSS 使用

## 方法一: 原生 dom 方法

使用原生的 dom 的方法来改变 css 的样式, 示例:

```javascript
document.getElementById(id).style.property = new style();
```

这里的 `new style` 里边就可以使用 js 传入的变量

此方法固然可以，但是对应改变一些复杂的 CSS,比如动画等，操作起来就不太方便了。此时以下方法就显得更为重要了.

---

## 方法二: CSS 变量

利用 CSS 变量来处理，思路是将 js 变量赋值给 css 变量，然后在 css 样式中使用 css 变量.

示例:

```javascript
// 设置变量
document.body.style.setProperty("--primary", "#7F583F");
// 读取变量
document.body.style.getPropertyValue("--primary").trim();
// '#7F583F'
// 删除变量
document.body.style.removeProperty("--primary");
```

```css
/* style 中直接声明css变量 */
body {
	--foo: #7f583f;
}
.content {
	--bar: #f7efd2;
}
```
