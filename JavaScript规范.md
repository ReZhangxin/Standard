# 语言规范

## 类型

- 基本类型
  - 字符串
  - 数值
  - 布尔类型
  - null
  - undefined
- 复杂类型
  - object
  - array
  - function

## 引用

`const` 和 `let` 都是块级作用域，`var` 是函数级作用域

对所有引用都使用 `const`，不要使用 `var`,如果引用是可变动的，则使用 `let`

```js
const arr = [1,3,5];
const person = {
  name:"张鑫",
  age:22
}
let num = 22;
if(num>22){
  num++;
}
```

## 对象

### 请使用字面量值创建对象

```js
const person = {
  name:"张鑫",
  age:22
}
```

### 使用对象**方法**的简写方式

```js
// 不推荐
const item = {
  value: 1,
  addValue: function (val) {
    return item.value + val
  }
}
// 推荐
const item = {
  value: 1,
  addValue(val) {
    return item.value + val
  }
}
```

### 请使用对象**属性值**的简写方式

```js
const job = "SB"
// bad
const item = {
  job: job
}
// good
const item = {
  job
}
```
## 数组

### 请使用字面量值创建数组

```js
// bad
const items = new Array()
// good
const items = []
```

### 向数组中添加元素时，请使用 `push` 方法

```js
const items = []
// bad
items[items.length] = 'test'
// good
items.push('test')
```

### 使用拓展运算符 `...` 复制数组

```js
// bad
const items = []
const itemsCopy = []
const len = items.length
let i
// bad
for (i = 0; i < len; i++) {
  itemsCopy[i] = items[i]
}
// good
itemsCopy = [...items]
```

### 使用数组的 `map` 等方法时，请使用 `return` 声明，如果是单一声明语句的情况，可省略 `return`

```js
// good
[1, 2, 3].map(x => {
  const y = x + 1
  return x * y
})
// good
[1, 2, 3].map(x => x + 1)
// bad
const flat = {}
[[0, 1], [2, 3], [4, 5]].reduce((memo, item, index) => {
  const flatten = memo.concat(item)
  flat[index] = flatten
})
// good
const flat = {}
[[0, 1], [2, 3], [4, 5]].reduce((memo, item, index) => {
  const flatten = memo.concat(item)
  flat[index] = flatten
  return flatten
})
// bad
inbox.filter((msg) => {
  const { subject, author } = msg
  if (subject === 'Mockingbird') {
    return author === 'Harper Lee'
  } else {
    return false
  }
})
// good
inbox.filter((msg) => {
  const { subject, author } = msg
  if (subject === 'Mockingbird') {
    return author === 'Harper Lee'
  }
  return false
})
```
