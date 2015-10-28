# 小小日记-桌面版

## 思考一

完全不懂GUI，所以需要一个教程来入门一下。  
- 本来准备用Udemy的一个关于PyQt的课程的，但是发现完全卡在了第一步安装上了。
- 改用python自带的Tkinter，先绕过安装的这个坑，开始练习再说。
- 搜索tkinter tuturial，选用了一个图文并茂并且看起来比较短的教程先学。
> 参考资料：[Python Tkinter](http://www.python-course.eu/python_tkinter.php)
- 发现时间不够用，所以先挑一些这次项目会用的相关章节先看。

## 思考二
#### 关于GUI
我希望我的GUI，有可爱的图片，字体好看一点啦。  
既然是GUI，就发挥一一下GUI图形界面里图形的作用。  
其实我觉得GUI就是要美美美，就是暂时实力还比较小白。

#### 关于网页交互
对网页交互这一块比较感兴趣，因为觉得网页端的跨平台性比较强，手机和电脑可以通用，而且也不用安装python就可以运行。  
这一部分有待发掘。

## 思考三
打开程序后，显示两个Button（带有图片显示）
- Write
- Read

Write版面
- 输入框
- 三个Button
    - Save
    - Read
    - Leave
    
Read版面
- 阅读框
- 一个Button
    - Write
    - 

## 尝试一
- 搜索read和write的图片，改成gif格式，宽度改成200
- 想使用带图片的button，google搜索，貌似和self.photo命令有关
- 搜到一段还有点类似的代码，button是在图片下，我觉得也可以
> 参考资料：[[Tutor] Images + Tkinter](https://mail.python.org/pipermail/tutor/2002-November/018610.html)
- 尝试着改一改，有个页面雏形
- 添加了中文，程序开始要添加一行```# -*- coding: utf-8 -*-```