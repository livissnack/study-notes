# CSS(Cascading Style Sheets:层叠样式表)

#### CSS定位(Positioning)
```
    css三种基本定位机制：普通流、浮动和绝对定位。
```

##### CSS定位属性
```
    css定位属性允许你对元素进行定位。
    1.position[把元素放置到一个静态的、相对的、绝对的、或固定的位置中。]
    2.top[	定义了一个定位元素的上外边距边界与其包含块上边界之间的偏移。]
    3.right[定义了定位元素右外边距边界与其包含块右边界之间的偏移。]
    4.bottom[定义了定位元素下外边距边界与其包含块下边界之间的偏移。]
    5.left[定义了定位元素左外边距边界与其包含块左边界之间的偏移。]
    6.overflow[设置当元素的内容溢出其区域时发生的事情。]
    7.clip[设置元素的形状。元素被剪入这个形状之中，然后显示出来。]
    8.vertical-align[设置元素的垂直对齐方式]
    9.z-index[设置元素的堆叠顺序。]
```

###### css的position属性：
```
    static：元素框正常生成。块级元素生成一个矩形框，作为文档流的一部分，行内元素则会创建一个或多个行框，置于其父元素中。
    relative：元素框偏移某个距离。元素仍保持其未定位前的形状，它原本所占的空间仍保留。
    absolute：元素框从文档流完全删除，并相对于其包含块定位。包含块可能是文档中的另一个元素或者是初始包含块。元素原先在正常文档流中所占的空间会关闭，就好像元素原来不存在一样。元素定位后生成一个块级框，而不论原来它在正常流中生成何种类型的框。
    fixed：元素框的表现类似于将 position 设置为 absolute，不过其包含块是视窗本身。
    提示：相对定位实际上被看作普通流定位模型的一部分，因为元素的位置相对于它在普通流中的位置。
```

###### CSS的相对定位
是设置为相对定位的元素框会偏移某个距离。元素仍然保持其未定位前的形状，它原本所占的空间仍保留。
```
    #box_relative {
      position: relative;
      left: 30px;
      top: 20px;
    }
```
*****
如下图所示：
![相对定位：relative](./Images/relative.gif)

###### CSS的绝对定位
绝对定位使元素的位置与文档流无关，因此不占据空间。这一点与相对定位不同，相对定位实际上被看作普通流定位模型的一部分，因为元素的位置相对于它在普通流中的位置。
```
    #box_relative {
      position: absolute;
      left: 30px;
      top: 20px;
    }
```

*****
如下图所示：
![绝对定位：absolute](./Images/absolute.gif)

###### CSS的浮动
右浮动：
![浮动：float](./Images/floating_right.gif)

*****
左浮动：
![浮动：float](./Images/floating_left1.gif)
*****
![浮动：float](./Images/floating_left2.gif)

#### CSS的Opacity属性
```
    opacity的值从0.0~1.0
```
    

#### CSS的单位
```
尺寸：
    1.百分比：%
    2.英寸：in
    3.em：1em 等于当前的字体尺寸。2em 等于当前字体尺寸的两倍。例如，如果某元素以 12pt 显示，那么 2em 是24pt。在 CSS 中，em 是非常有用的单位，因为它可以自动适应用户所使用的字体。
    4.ex：一个 ex 是一个字体的 x-height。 (x-height 通常是字体尺寸的一半。)
    5.pt: 磅 (1 pt 等于 1/72 英寸)
    6.pc: 12 点活字 (1 pc 等于 12 点)
    7.px: 像素 (计算机屏幕上的一个点)
颜色：
    rgb(x,x,x): RGB 值 (比如 rgb(255,0,0))
    rgb(x%, x%, x%): RGB 百分比值 (比如 rgb(100%,0%,0%))
    #rrggbb: 十六进制数 (比如 #ff0000)
```

#### CSS的颜色名
```
    HTML和CSS颜色规范中定义了147中颜色名（17种标准颜色加130种其他颜色）
    17种标准色是：
        aqua,
        black,
        blue,
        fuchsia,
        gray,
        green,
        lime,
        maroon,
        navy,
        olive,
        orange,
        purple,
        red,
        silver,
        teal,
        white,
        yellow
```