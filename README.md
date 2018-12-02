# CSS3
布局方式、照片墙、半像素、3d、animation、progress、transform、轮播图等
- -webkit-font-smoothing它有三个属性值：

none：对低像素的文本比较好

subpixel-antialiased：默认值

antialiased：抗锯齿很好 

例子：


<html>
body{
   -webkit-font-smoothing: antialiased;
}
</html>


这个属性可以使页面上的字体抗锯齿,使用后字体看起来会更清晰。加上之后就顿时感觉页面小清晰了。

- Gecko也推出了自己的抗锯齿效果的非标定义。

-moz-osx-font-smoothing: inherit | grayscale;


###### white-space:nowrap

溢出显示省略号


<html>
<head>
    <meta charset="UTF-8">
    <title>.5px</title>
    <style>


        *{
            margin: 0;
            padding: 0;
        }
        .box{
            width: 100px;
            height: 100px;
            background: #e5a8de;
            /*border: 1px dashed #e572df;*/
            /*transform: scale(0.5);*/
            /*transform-origin: 0 0;*/
        }
        .box::after{
            content: "";
            display: block;
            width: 200px;
            height: 200px;
            border: 1px solid #89eff2;
            /*transform: scale(0.5) ;*/

            /*transform-origin: 0 0;*/
            /*存在大小空隙*/
            /*用怪异盒模型转化*/
            /*box-sizing: border-box; */



        }
    </style>
</head>
<body>
    <div class="box"></div>
</body>
</html>

#### WEB——0.5半像素实现：
###### 两种方法：
- 通过transform: scale(0.5);进行缩放；
- 转化为怪异盒模型box-sizing: border-box; 

- px相对单位——相对物理显示屏；
- em相对单位——相对于font-size,有自己的相对于自己的，没有就相对于父级的；
- font-size存在最小值；默认16px；一般不小于14px；
- rem中的r表示root,HTML的根节点是HTML，相对于根节点定位；

- 主题切换引入CSS文件；
- pageshow和onload都是监听页面加载，但pageshow与缓存无关，每次都加载，onload存在缓存触发问题；
- boostrap
- orientation:landscape(横屏)； orientation:portrait（竖屏）；
- 物理像素比dpr一定要加webkit前缀；

