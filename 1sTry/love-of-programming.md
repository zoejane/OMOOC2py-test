# 让编程更有爱的一点 - 继续小小日记

>更新日志
>20151020 创建
## 小小日记任务回顾

- 完成一个极简交互式日记系统，需求如下：
	- 一次接收输入一行日记
	- 保存为本地文件
	- 再次运行系统时,能打印出过往的所有日记
- 第一次笔记
    - [小小日记系统-第一次尝试](https://zoejane.gitbooks.io/omooc2py/content/1sTry/diary101.html)
	
## 思考二

看issue回复的时候，觉得是不是还是在py里面进行互动和输入会更好一些？  
这样界面会更友好，提示性也更强一些，  
不会出现我自己过了好久都不记得怎么用的情况，  
别人用起来也觉得一目了然，不用去翻帮助文档。

同时，互动文字可以让程序更有爱一些。  
感觉好像有一个人在和你对话，而不是硬邦邦的代码。  
记得看那本和game有关的python的书时，最打动我的就是它的举例的程序，运用的互动语言都很有感情，让我觉得编程原来也可以是这么有感情的事。

- 输入diary.py
- 出现提示：
    - Hi. I am the diary of yours.
    - Do you have something want to share with me now?
    - Or you can just press Enter to read all of me.
- open file 'diary' , append mode
- newDiary=input()
- 出现提示：
    - Thank you for sharing with me.
    - Bye. I will miss you.
- close file


#### 尝试四：

感觉大家还是使用python2的比较多。  
所以这次编程准备在python2.7的环境下编写。

##### Question
- input() not working in python2
- 没发现中文有什么问题呀，大妈说的中文输入问题到底指的是什么呢？

##### Solution

>Use raw_input() instead of input():  
```testVar = raw_input("Ask user for something.")```  
input() actually evaluates the input as Python code.   
I suggest to never use it.  
raw_input() returns the verbatim string entered by the user.

>Although for anyone reading this using Python 3, input now works this way, and raw_input is gone.

> via [Python 2.7 getting user input and manipulating as string without quotations](http://stackoverflow.com/questions/4960208/python-2-7-getting-user-input-and-manipulating-as-string-without-quotations)


## 思考三

再次受到issue的启发，  
包括那时候上Kunal的课，其实最感动的是，当他们用python写出一些很简单但充满爱的小程序，和他们所爱的人一起分享的时刻。  
无论是给自己的小孩子上一课超简单的python课，还是用python做出一个小小照片游戏，告诉自己亲爱的人，说爱你。  
我想，这是我觉得python最有爱的时刻，也是最最让我感动的时刻。  
这程序