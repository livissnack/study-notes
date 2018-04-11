### XML
##### XML简介

```
    可扩展标记语言，标准通用标记语言的子集，是一种用于标记电子文件使其具有结构性的标记语言。
    设计宗旨是用来传输和存取数据的，而不是用来显示数据的。
```

##### XML语法
- 所有XML元素都须有关闭标签
###### 在HTML，经常会看到没有关闭标签的元素：

    ```
        <p>This is a paragraph
        <p>This is another paragraph
    ```
###### 在XML中，省略关闭标签是非法的。所有元素都必须有关闭标签：

    ```
        <p>This is a paragraph</p>
        <p>This is another paragraph</p>  
        注释：您也许已经注意到 XML 声明没有关闭标签。这不是错误。声明不属于XML本身的组成部分。它不是 XML 元素，也不需要关闭标签。
    ```
- XML标签对大小写敏感
- XML必须正确地嵌套
- XML文档必须有根元素
- XML的属性值须加引号
- 实体引用
- XML中的注释
- 在XML中，空格会被保留
- XML以LF存储换行
