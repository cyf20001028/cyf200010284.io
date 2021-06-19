#                          css学习总结

##  一 css概述

1. CSS：层叠样式表（Cascading Style Sheets）用于渲染HTML元素标签的样式，美化网页的一门技术 。使用CSS设置样式，可以让展示数据的HTML代码和设置样式的CSS代码进行分离，可以增强网页的展示能力
2. 一条CSS样式规则由两个主要的部分构成：选择器，以`{}`包裹的一条或多条声明:<img src="D:\weblearn1\images\EL69DQN_L_[0Z6VR7KJD0TU.png" style="zoom:80%;" />

​       选择器通常是需要改变样式的HTML元素

​       每条声明由一个属性和一个值组成。

​       属性（property）是希望设置的样式属性（style attribute）。每个属性有一个值。属性和值被冒号分开。

## 二 css如何导入HTML

###      1.通过外部样式表

​           当css的代码特别多的时候，可以将css写入一个独立文件中，文件如xxx/xx.css

```
<link rel="stylesheet"  href="css/cyf20001028.css"/>
```



###      2.内部样式表

​       第二种方式是通过head标签内部的style标签，书写CSS代码来引入CSS样式。

​    

```
<style type="text/css">
  span{
       border:2px solid :cyan;
       font-site:35px;
       font-weight:bolder
  }
  </tyle>
```



### 三.选择器

​     1.id 选择器

> id 选择器可以为标有特定 id 的 HTML 元素指定特定的样式。
>
> HTML元素以id属性来设置id选择器,CSS 中 id 选择器以 “#” 来定义。
>
> 以下的样式规则应用于元素属性 id=“para1”:

![MNLZYKXG48BQLJBF)TP{VB3](D:\weblearn1\images\MNLZYKXG48BQLJBF)TP{VB3.png)

 2.class 选择器

class 选择器用于描述一组元素的样式，class 选择器有别于id选择器，class可以在多个元素中使用。

class 选择器在HTML中以class属性表示, 在 CSS 中，类选择器以一个点"."号显示：

在以下的例子中，所有拥有 center 类的 HTML 元素均为居中。
![](D:\weblearn1\images\AOEY{Q6MI]4XFR$]03`63)9.png)

## 四.盒子模型

所谓盒子模型，在HTML里，所有页面元素都可以看成一个一个的框（盒子），这些元素与元素之间的距离，元素的边框，元素与元素之间的距离都会影响元素的位置和元素本身的宽和高。

![](D:\weblearn1\images\{9U03`[HFWCHV]3@5FXYMMI.png)

- Content(内容）盒子的内容，如文本、图片等

- Padding(内边距) 清除内容周围的区域，内边距是透明度

- Border(边框)  围绕在内边距和内容外的边框。

- Margin(外边距)-清除边框外的区域，外边距是透明的。

  1. **<u>需要注意的是：元素和元素之间的距离叫做外边距，当两个元素在垂直方向的外边距相遇时将会有合并的现象，合并后的结果是，取两个外边距之中的较大者来作为两个元素的外边距！</u>**

  2. **<u>元素的实际宽度=元素设置的宽度+元素的左右边框宽度+左右内边距+左右外边距</u>**

  3. **<u>元素的实际高度=蒜素设置的高度+元素的上下边框宽度+上下内边距+上下外边距</u>**

     ## 五.定位

     [static]：默认值，没定位。

     [fixed]：相对于浏览器窗口是固定位置，即使窗口是滚动的它也不会移动。

     [relative]：相对定位元素的定位是相对其正常位置。

     [absolute]：绝对定位的元素的位置相对于最近的已定位父元素，如果元素没有已定位的父元素，那么他的位置相对于<html>

     [sticky] :粘性定位，依赖于用户的滚动，在绝对与相对之间切换

     ## 六.浮动

     CSS 的 Float（浮动），会使元素向左或向右移动，其周围的元素也会重新排列。

     Float（浮动），往往是用于图像，但它在布局时一样非常有用。

     ```
     <html>
     <head>
        <style>
          .example-float-right {
          float:right;
          }
          </stype>
          </head>
          <body>
          <imy src "https://mdbootstrap.com/img/photos/others/placelder1.jpg">
          <p>浮动</p>
          </body>
          </html>
     ```

     

  清除浮动

    

  ```
  .clearfix:after{
              content:".";
              visibility:hidden;
              display:block;
              height:0;
              clear:both;
  }
  ```

  ##     七.伪类与伪函数

  ​     随着CSS规范进一步完善，新增的CSS伪元素越来越多，但是在日常开发中，我们常用的及浏览器支持情况比较乐观的当数before和after，伪类和伪元素没有做出区分，都是使用一个冒号；

> ***伪类***
>
> - a链接样式
> - 隔行变色
>
> ***伪元素***
>
> - 最常见的使用伪元素after清除浮动
> - 实现按钮文字隐藏
> - 首行、首字母样式

## 八.不透明度

opacity:不透明度

属性参数的＂不透明度＂是以数字表示，从 0.0 至 1.0 都可以，完全透明是 0.0，完全不透明是 1.0，数字越大代表元素越不透明。参数除了可以使用＂不透明度＂之外，还有 inherit 继承父层属性，不过浏览器支援度较差。代码如下：

```
<html>
<head>
  .opacity-2{
  opacity:0.3;
  }
  .opacity-5{
  opacity:05;
  }
  .opacity-7{
  opacity：1；
  }
  </style>
  </head>
  <body>
  <img class="opacity-2" src="https://xxx.com/xx.jpg">
  <img class="opacity-2" src="https://xxx.com/xx.jpg">
  <img class="opacity-2" src="https://xxx.com/xx.jpg">
  </body>
  </html>
```

