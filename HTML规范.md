# HTML 规范

## HTML5标准模板

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<title>HTML5标准模版</title>
</head>
<body>
	
</body>
</html>
```

## 移动端

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, shrink-to-fit=no" >
<meta name="format-detection" content="telephone=no" >
<title>移动端HTML模版</title>
	
<!-- S DNS预解析 -->
<link rel="dns-prefetch" href="">
<!-- E DNS预解析 --> 
<!-- S 线上样式页面片，开发请直接取消注释引用 -->
<!-- #include virtual="" -->
<!-- E 线上样式页面片 -->
<!-- S 本地调试，根据开发模式选择调试方式，请开发删除 --> 
<link rel="stylesheet" href="css/index.css" >
<!-- /本地调试方式 -->
<link rel="stylesheet" href="http://srcPath/index.css" >
<!-- /开发机调试方式 -->
<!-- E 本地调试 -->
</head>
<body>
</body>
</html>
```

## PC端

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="keywords" content="your keywords">
<meta name="description" content="your description">
<meta name="author" content="author,email address">
<meta name="robots" content="index,follow">
<meta http-equiv="X-UA-Compatible" content="IE=Edge,chrome=1">
<meta name="renderer" content="ie-stand">
<title>PC端HTML模版</title>
<!-- S DNS预解析 --> 
<link rel="dns-prefetch" href="">
<!-- E DNS预解析 --> 
<!-- S 线上样式页面片，开发请直接取消注释引用 -->
<!-- #include virtual="" -->
<!-- E 线上样式页面片 -->
<!-- S 本地调试，根据开发模式选择调试方式，请开发删除 --> 
<link rel="stylesheet" href="css/index.css" >
<!-- /本地调试方式 -->
<link rel="stylesheet" href="http://srcPath/index.css" >
<!-- /开发机调试方式 -->
<!-- E 本地调试 -->
</head>
<body>
</body>
</html>
``` 

## 代码规范

- 所有具有开始标签和结束标签的元素都要写上起止标签，某些允许省略开始标签或和束标签的元素亦都要写上。

- 空元素标签都不加 “/” 字符

```html
<div>
    <h1>我是h1标题</h1>
    <p>我是一段文字，我有始有终，浏览器能正确解析</p>
</div>
	
<br>
```

### 书写规则

- `HTML`代码大小写
- `HTML`标签名、类名、标签属性和大部分属性值统一用小写

```html
<div class="demo"></div>
```
### 类型属性

不需要为 `CSS`、`JS` 指定类型属性，`HTML5` 中默认已包含


```html
<!-- 推荐：-->
<link rel="stylesheet" href="" >
<script src=""></script>

<!-- 不推荐：-->
<link rel="stylesheet" type="text/css" href="" >
<script type="text/javascript" src="" ></script>
```

### 元素属性

- 元素属性值使用双引号语法
- 元素属性值可以写上的都写上

```html
<!-- 推荐：-->

<input type="text">
<input type="radio" name="name" checked="checked" >

<!-- 不推荐：-->
<input type=text>	
<input type='text'>
<input type="radio" name="name" checked >
```

### 特殊字符引用

- 文本可以和字符引用混合出现。这种方法可以用来转义在文本中不能合法出现的字符。
- 在 HTML 中不能使用小于号 “<” 和大于号 “>”特殊字符，浏览器会将它们作为标签解析，若要正确显示，在 HTML 源代码中使用字符实体

```html
<!-- 推荐：-->
<a href="#">more&gt;&gt;</a>

<!-- 不推荐：-->
<a href="#">more>></a>
```

### 代码缩进

- 统一使用四个空格进行代码缩进，使得各编辑器表现一致（各编辑器有相关配置）

```html
<div class="jdc">
    <a href="#"></a>
</div>
```

### 纯数字输入框

使用 type="tel" 而不是 type="number"

```html
<input type="tel">
```

## 注释规范

### 单行注释

一般用于简单的描述，如某些状态描述、属性描述等

注释内容前后各一个空格字符，注释位于要注释代码的上面，单独占一行

```html
<!-- Comment Text -->
<div>...</div>
```














