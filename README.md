# Standard
制定一套自己遇到的规范

## 关于注释问题

> 如果是中文全部用中文，标点符号也用中文 ；不要 中文注释标点符号却是英文版。

## 关于html，body样式

```css
/*html没有margin和padding body只有margin没有padding*/
html{font-family:"Comic Sans MS";box-sizing:border-box;font-size:10px;}
*,*:before,*:after{box-sizing:inherit;}
body{margin:0;}
/*rem根据html设置的font-size大小 1rem=10px*/
div{font-size:1.2rem;}
```
