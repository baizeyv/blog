+++
date = '2026-04-04T13:35:01+08:00'
draft = false
title = 'Assign Js to Css'
tags = ['Javascript', 'Css']
+++

# Assigning JavaScript Variables for Use in CSS

## Way 1: Native DOM Methods

Using native DOM methods to modify CSS styles, for example:

```javascript
document.getElementById(id).style.property = new style();
```

Within this `new style` block, you can utilize variables passed in from JavaScript.

While this approach certainly works, it becomes rather cumbersome when dealing with more complex CSS modifications—such as animations. In such scenarios, the method described below proves to be far more essential.

---

## Way 2: CSS Variable

The approach involves utilizing CSS variables: assign the value of a JavaScript variable to a CSS variable, and then use that CSS variable within your CSS styles.

for example:

```javascript
// set variable
document.body.style.setProperty("--primary", "#7F583F");
// get variable
document.body.style.getPropertyValue("--primary").trim();
// '#7F583F'
// remove variable
document.body.style.removeProperty("--primary");
```

```css
/* Declaring CSS variables directly within the style block */
body {
	--foo: #7f583f;
}
.content {
	--bar: #f7efd2;
}
```
