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

##### 代码
```
import time

print('Hi, I am the diary of yours.')
print('Do you have something want to share with me now?')
print('Or you can just press Enter to read all of me.')

diary = raw_input('>>')

if diary == '':
    diaryFile = open('diary.txt')
    diary = diaryFile.read()
    print(diary)
    
else:
    diaryFile = open('diary.txt','a')
    diaryFile.write('\n' + time.strftime('%Y/%m/%d')+ ' ' +diary)

    print('Thank you for sharing with me.')
    print('Bye. I will miss you.')

diaryFile.close()
```

## 思考三

再次受到issue的启发，  
包括那时候上Kunal的课，其实最感动的是，当他们用python写出一些很简单但充满爱的小程序，和他们所爱的人一起分享的时刻。  
无论是给自己的小孩子上一课超简单的python课，还是用python做出一个小小照片游戏，告诉自己亲爱的人，说爱你。  
我想，这是我觉得python最有爱的时刻，也是最最让我感动的时刻。  
那些程序是那样的简单，却让我真的感觉到，这样简单的事情是如此的有意义。

我想，为什么要把编程这件事搞得好像那么深奥和复杂呢，好像难以和不了解编程的人沟通呢？  
想起之前都是自己在这里看视频，学写代码，感觉好像也不知道怎么和老公说这件事情一样，为什么不用一种别的形式来一起分享这个过程呢？  
包括他问起来我写了些什么，我好像一下子也难以描述清楚。  
为什么不把这件事情从自娱自乐，转变成和他一起来分享呢？  
虽然我自己也觉得好玩啦，不过是不是之前根本没这么想过？  
是这件事情很难，还是我根本没有尝试过呢？

失败也没有关系啦，起码我也可以看看他的反馈，自己再改进嘛。  
而且我觉得这样应该还蛮好玩的。  

喵，好高兴今天突然想起了那时候Kunal传达给我的这种充满爱的感觉。  
让我感觉，编程就是生活的一部分，编程让生命更有爱。  
编程不仅仅是关于计算机，更是关于人，关于我所爱的人。  

About People.   
About Love.   
About Life.  

Zoe, remember this feeling.

#### 尝试五 - Special Version for 哥哥

- 这次界面要用中文写啦。 

##### Question
- 才发现mac下的idle是不能写中文的...

#### Solution
>[mac下的 idle为何不能输入中文?该如何解决?](http://www.zhihu.com/question/26532408)  
第一种情况是在 IDLE 下中文输入法失效。这是因为 IDLE 界面使用的 Tkinter 需要依赖 Tcl/Tk，而系统自带的 Tcl/Tk 版本太低，造成了不兼容的问题。   
可以用homebrew安装 ```brew install tcl-tk```