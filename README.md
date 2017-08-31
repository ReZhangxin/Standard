# Standard
制定一套自己遇到的规范

## 1.关于注释问题

> 如果是中文全部用中文，标点符号也用中文 ；不要 中文注释标点符号却是英文版。

## 2.关于html，body样式

```css
/*html没有margin和padding body只有margin没有padding*/
html{font-family:"Comic Sans MS";box-sizing:border-box;font-size:10px;}
*,*:before,*:after{box-sizing:inherit;}
body{margin:0;}
/*rem根据html设置的font-size大小 1rem=10px*/
div{font-size:1.2rem;}
```

## 3.关于单行文本超出省略，多行文本超出省略，在手机端单、多行文本超出省略

```css
element
{
  width:3erm;overflow: hidden;text-overflow: ellipsis;white-space: nowrap;/*可继承不可内联*/
}
/*移动端*/
element
{
  overflow : hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
}
/*兼容*/
element{
    position: relative;
    line-height: 1.4em;
    /* 4 times the line-height to show 4 lines */
    height: 5.6em;
}
p::after {
    content: "...";
    font-weight: bold;
    position: absolute;
    bottom: 0;
    right: 0;
    padding: 0 20px 1px 45px;
}
```
