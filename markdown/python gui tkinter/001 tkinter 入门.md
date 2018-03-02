# python GUI tkinter


Python 提供了多个图形开发界面的库，几个常用的Python GUI库如下：
Tkinter：wxPython：Jython：

首先，我想由官方库Tkinter入手。虽然听说官方库功能不是很强，很多文章都推荐由wxPython开始学习。但我想，既然Tkinter被认作官方库，也必然由其原有吧。就算以后不用，至少了解一下也没什么坏处。

所用脚本都在python3.6下测试成功. 

创建一个GUI程序：
1. 导入Tkinter模块
2. 创建控件
3. 指定这个控件的master，即这个控件属于哪一个
4. 告诉GM（geometry manager）有一个控件产生了

注意： Python3.x 版本使用的库名为 tkinter,即首写字母 T 为小写。

```
#!/usr/bin/python
# -*- coding: UTF-8 -*-
import tkinter         #加载模块
top = tkinter.Tk()    
top.mainloop() #进入消息循环
```


![MWSnap198.jpg](http://upload-images.jianshu.io/upload_images/10113743-6c35b1d574fd51c3.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```python
# -*- coding:UTF-8 -*- 
import tkinter   #导入tkinter库 
	root = tkinter.Tk() 
li = ['C','python','php','html','SQL','java']        #创建列表li
movie = ['CSS','jQuery','Bootstrap']    #创建列表movie
listb = tkinter.Listbox(root)    #创建列表窗口
listb2 = tkinter.Listbox(root)     #创建列表窗口
for item in li:    #在列表窗口内填入列表内容
  	listb.insert(0,item) 
for item in movie: 
	listb2.insert(0,item)
listb.pack()     #pack函数是布局函数
listb2.pack() 
root.mainloop()
```
![MWSnap199.jpg](http://upload-images.jianshu.io/upload_images/10113743-0c29caa2f816b744.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

改变窗口的名字的两种方法：

```python
#第一种方法
from tkinter import *
root = Tk()
root.title("窗口标题") #在这里修改窗口的标题
root.mainloop()
```
![运行结果](http://upload-images.jianshu.io/upload_images/10113743-78c0d5582c5bd0b1.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```python
#第二种方法
from tkinter import *
root = Tk(className = '窗口标题2')
root.mainloop()
```
![运行结果](http://upload-images.jianshu.io/upload_images/10113743-3ee0edfa3db2a325.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)






