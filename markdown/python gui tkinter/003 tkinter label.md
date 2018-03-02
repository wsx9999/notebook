# 003. tkinter label

abel  是标签控件；可以显示文本和位图

###Lable 标签


```python
Label=Tkinter.Lable(master,text=’helloworld!’)
```

#属性：
###master
说明： 指定控件的父窗口
###text
说明：要显示的文字
```Label=Tkinter.Lable(master,text=’helloworld!’)```
###wraplength
说明：指定text中文本多少宽度后开始换行
```label=Tkinter.Label(root,text='abcdefghijklmnopqrstuvwxyz', wraplength=50)```
###justify
说明：text中多行文本的对齐方式
```python
label=Tkinter.Label(root,text='abcdefghikjlmnopqrstuvwxyz',wraplength=50,justify='left')
label=Tkinter.Label(root,text='abcdefghikjlmnopqrstuvwxyz',wraplength=50,justify='right')
label=Tkinter.Label(root,text='abcdefghikjlmnopqrstuvwxyz', wraplength=50, justify='center')
```
###anchor
说明：文本（text）或图像（bitmap/image）在Label的位置。默认为center
值和布局：

```
               nw        n         ne

               w       center      e

               sw        s          se
```

```python
label=Tkinter.Label(root,text='abcdefghikjlmnopqrstu',wraplength=50,width=30,height=10, bg='blue',fg='red',anchor='nw')
```

###bitmap
说明： 显示内置位图。如果image选项被指定了，则这个选项被忽略。下面的位图在所有平台上都有效：

> error, gray75, gray50, gray25, gray12, hourglass, info, questhead, question,  warning。

![位图](http://upload-images.jianshu.io/upload_images/10113743-60ea3b435ce2b2d5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

###fg  bg
说明：设置前景色和背景色
```label=Tkinter.Label(root,text='helloworld!',fg='red',bg='blue')```

1. 使用颜色名称 Red Green Blue Yellow LightBlue ...... 
2. 使用#RRGGBB  label = Label(root,fg = 'red',bg ='#FF00FF',text = 'Hello I am Tkinter') 指定背景色为绯红色 
3. 除此之外，Tk还支持与OS相关的颜色值，如Windows支持SystemActiveBorder,  SystemActiveCaption,  SystemAppWorkspace,  SystemBackground, .....

###width height
说明：设置宽度和高度
label=Tkinter.Label(root,text='helloworld!',fg='red',bg='blue',width=50,height=10)

###compound
说明：指定文本(text)与图像(bitmap/image)是如何在Label上显示，缺省为None，当指定image/bitmap时，文本(text)将被覆盖，只显示图像了。

    可以使用的值：
    left：        图像居左
    right:        图像居右
    top：         图像居上
    bottom：      图像居下     
    enter：       文字覆盖在图像上

```label=Tkinter.Label(root,text='error',bitmap='error', compound='left')```

##以下是关于label调用的实例:

一个显示三个label的窗口, 其中width命令调整该label的宽度, height调整该label的高度. 

```python
from tkinter import *
root = Tk()
one = Label(root, text = 'helloworld', width = 30, height = 3)
one.pack()

two = Label(root, text = 'helloworld')
two['width'] = 30
two['height'] = 3
two.pack()

three = Label(root, text = 'helloworld')
three.pack()
three.configure(width =  30, height = 3)
three.pack()
```
以上三个实例中, 分别用三种方式调整label的长度和宽度, 其结果是相同的.
第一种方法: 直接在创建对象时, 指定label的长度和宽度
第二种方法: 使用属性wight和height指定label的长度和宽度
第三种方法: 使用configure或config方法指定label的长度和宽度
![运行结果](http://upload-images.jianshu.io/upload_images/10113743-e667d022425c70cf.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)





