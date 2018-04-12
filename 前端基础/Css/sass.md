### SASS基础教程
- sass简介
sass有两种后缀名文件：一种后缀名为sass，不使用大括号和分号；
另一种就是我们这里使用的scss文件，这种和我们平时写的css文件
格式差不多，使用大括号和分号。而本教程中所说的所有sass文件都
指后缀名为scss的文件。在此也建议使用后缀名为scss的文件，以
避免sass后缀名的严格格式要求报错。
```
    //文件后缀名为sass的语法
    body
      background: #eee
      font-size:12px
    p
      background: #0982c1
      
    
    //文件后缀名为scss的语法  
    body {
      background: #eee;
      font-size:12px;
    }
    p{
      background: #0982c1;
    } 
```

- sass入门
```
    变量
    sass中可以定义变量，方便统一修改和维护。
```
```
    //sass style
    //-----------------------------------
    $fontStack:    Helvetica, sans-serif;
    $primaryColor: #333;
    
    body {
      font-family: $fontStack;
      color: $primaryColor;
    }
```
```
    //css style
    //-----------------------------------
    body {
      font-family: Helvetica, sans-serif;
      color: #333;
    }
```

*****

```
    嵌套
    sass可以进行选择器的嵌套，表示层级关系，看起来很优雅整齐。
```
```
    //sass style
    //-----------------------------------
    nav {
      ul {
        margin: 0;
        padding: 0;
        list-style: none;
      }
    
      li { display: inline-block; }
    
      a {
        display: block;
        padding: 6px 12px;
        text-decoration: none;
      }
    }
```
```
   //css style
   //-----------------------------------
   nav ul {
     margin: 0;
     padding: 0;
     list-style: none;
   }
   
   nav li {
     display: inline-block;
   }
   
   nav a {
     display: block;
     padding: 6px 12px;
     text-decoration: none;
   }
```


*****

```
    导入
    sass中如导入其他sass文件，最后编译为一个css文件，优于纯css的 @import
```
```
    //sass style
    //-----------------------------------
    // _reset.scss
    
    html,
    body,
    ul,
    ol {
       margin: 0;
      padding: 0;
    }
```
```
  //sass style
  //-----------------------------------
  // base.scss 
  
  @import 'reset';
  
  body {
    font-size: 100% Helvetica, sans-serif;
    background-color: #efefef;
  }
```
```
    //css style
    //-----------------------------------
    html, body, ul, ol {
      margin: 0;
      padding: 0;
    }
    
    body {
      background-color: #efefef;
      font-size: 100% Helvetica, sans-serif;
    }
```

*****

```
    mixin
    sass中可用mixin定义一些代码片段，且可传参数，方便日后根据需求调用。从此处理css3的前缀兼容轻松便捷。
```
```
    //sass style
    //-----------------------------------
    @mixin box-sizing ($sizing) {
        -webkit-box-sizing:$sizing;     
           -moz-box-sizing:$sizing;
                box-sizing:$sizing;
    }
    .box-border{
        border:1px solid #ccc;
        @include box-sizing(border-box);
    }
```
```
    //css style
    //-----------------------------------
    .box-border {
      border: 1px solid #ccc;
      -webkit-box-sizing: border-box;
      -moz-box-sizing: border-box;
      box-sizing: border-box;
    }
```

*****

```
    扩展/继承
    sass可通过 @extend来实现代码组合声明，使代码更加优越简洁。
```
```
    //sass style
    //-----------------------------------
    .message {
      border: 1px solid #ccc;
      padding: 10px;
      color: #333;
    }
    
    .success {
      @extend .message;
      border-color: green;
    }
    
    .error {
      @extend .message;
      border-color: red;
    }
    
    .warning {
      @extend .message;
      border-color: yellow;
    }
```
```
    //css style
    //-----------------------------------
    .message, .success, .error, .warning {
      border: 1px solid #cccccc;
      padding: 10px;
      color: #333;
    }
    
    .success {
      border-color: green;
    }
    
    .error {
      border-color: red;
    }
    
    .warning {
      border-color: yellow;
    }
```


*****

```
    运算
    sass可进行简单的加减乘除运算等
```
```
    //sass style
    //-----------------------------------
    .container { width: 100%; }
    
    article[role="main"] {
      float: left;
      width: 600px / 960px * 100%;
    }
    
    aside[role="complimentary"] {
      float: right;
      width: 300px / 960px * 100%;
    }
```
```
   //css style
   //-----------------------------------
   .container {
     width: 100%;
   }
   
   article[role="main"] {
     float: left;
     width: 62.5%;
   }
   
   aside[role="complimentary"] {
     float: right;
     width: 31.25%;
   }
```

*****

```
    颜色
    sass中集成了大量的颜色函数，让变换颜色更加简单。
```
```
    //sass style
    //-----------------------------------
    $linkColor: #08c;
    a {
        text-decoration:none;
        color:$linkColor;
        &:hover{
          color:darken($linkColor,10%);
        }
    }
```
```
   //css style
   //-----------------------------------
   a {
     text-decoration: none;
     color: #0088cc;
   }
   a:hover {
     color: #006699;
   }
```