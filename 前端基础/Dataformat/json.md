### JSON
##### JSON简介
```
    JSON(JavaScript Object Notation, JS 对象标记) 是一种轻量级的数据交换格式。
    它基于 ECMAScript (欧洲计算机协会制定的js规范)的一个子集，采用完全独立于编程
    语言的文本格式来存储和表示数据。简洁和清晰的层次结构使得 JSON 成为理想的数据交
    换语言。 易于人阅读和编写，同时也易于机器解析和生成，并有效地提升网络传输效率。
```
##### JSON语法规则

`在 JS 语言中，一切都是对象。因此，任何支持的类型都可以通过 JSON 来表示，例如字符串、数字、对象、数组等。但是对象和数组是比较特殊且常用的两种类型：`
   
- 对象表示为键值对
- 数据由逗号分隔
- 花括号保存对象
- 方括号保存数组

##### JSON键/值对
`JSON 键值对是用来保存 JS 对象的一种方式，和 JS 对象的写法也大同小异，键/值对组合中的键名写在前面并用双引号 "" 包裹，使用冒号 : 分隔，然后紧接着值：`
> {"firstName": "Json"}

##### JSON和JS对象互转
```
    要实现从对象转换为 JSON 字符串，使用 JSON.stringify() 方法：
    var json = JSON.stringify({a: 'Hello', b: 'World'}); //结果是 '{"a": "Hello", "b": "World"}'
```

```
    要实现从 JSON 转换为对象，使用 JSON.parse() 方法：
    var obj = JSON.parse('{"a": "Hello", "b": "World"}'); //结果是 {a: 'Hello', b: 'World'}
```

