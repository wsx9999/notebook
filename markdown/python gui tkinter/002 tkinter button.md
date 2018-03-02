# 002. tkinter button

### 用python构建button组件的方法

```python
from tkinter import *  #载入tkinter模块
root = Tk()

def helloButton():  #构建button执行动作
  print('Hello Button!')

Button(root, text = 'Hello Button!', command = helloButton).pack()

root.mainloop()
```
![输出样式](http://upload-images.jianshu.io/upload_images/10113743-fb762654ca341173.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


```python
from tkinter import * #导入tkinter库

root = Tk()

def helloButton():  #构建button执行动作
  print('Hello Button!')

#设置button样式
Button(root, text = 'hello button',command = helloButton,relief = FLAT).pack()
Button(root, text = 'hello button',command = helloButton,relief = GROOVE).pack()
Button(root, text = 'hello button',command = helloButton,relief = RAISED).pack()
Button(root, text = 'hello button',command = helloButton,relief = SOLID).pack()
Button(root, text = 'hello button',command = helloButton,relief = SUNKEN).pack()

root.mainloop()
```
![输出样式](http://upload-images.jianshu.io/upload_images/10113743-a4690d8b562cefd0.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



```python
from tkinter import * #导入tkinter库

root = Tk()

Button(root, text='botton', compound='bottom', bitmap='error').pack()  
Button(root, text='top', compound='top', bitmap='error').pack()  
Button(root, text='right', compound='right', bitmap='error').pack()  
Button(root, text='left', compound='left', bitmap='error').pack()  
Button(root, text='center', compound='center', bitmap='error').pack()  

root.mainloop()
```
![输出样式](http://upload-images.jianshu.io/upload_images/10113743-cdbc19cb73ac41bf.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 使button加载位图

```python
# -*- coding:UTF-8 -*-
from tkinter import *  #载入tkinter模块
root = Tk()
img = PhotoImage(file = 'd:/1.gif')  #如果和主程序不在同一文件夹下，则需要写入详细路径，如果和主程序在同一文件夹下，则只需要写文件名。如果在主程序所在的文件夹内的子文件夹内，则可以写’./****/**.gif‘
button = Button(root,image = img)
button.pack()
root.mainloop()
```
![输出样式](http://upload-images.jianshu.io/upload_images/10113743-9e66243bcc5de1d9.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

