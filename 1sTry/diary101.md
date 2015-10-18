# 交互101 - 小小日记系统

## 卡片一：本周整体任务概述:

- 完成一个极简交互式日记系统，需求如下：
	- 一次接收输入一行日记
	- 保存为本地文件
	- 再次运行系统时,能打印出过往的所有日记
- 时限: 0wd4~1wd3
- 发布: 发布到各自仓库的 _src/om2py0w/0wex1/ 目录中
- 指标:
	- 包含软件使用说明书: README.md
	- 能令其它学员根据说明书,运行系统,完成所有功能

## 思考一：

-  输入“diary.py 日记内容”，将内容保存为本地文件
- 要用到import sys的sys.argv
	- if len(sys.argv) >1：（含有日记内容）
		- 输入一行文字到diary.txt
		- 如果diary.txt不存在，创建它
- 输入‘diary.py’，打印以往所有日记
	- if len(sys.argv) >1：
		- 打开diary.txt	 
		- 如果diary.txt不存在，创建它

#### Question

- 如何用python创建diary.txt
- 如何用python添加文字到某一个文档

#### Solution

- 学习 [Lesson31 Reading and Writing Plaintext Files@Automate](https://www.udemy.com/automate/learn/#/lecture/3470542)
    - append mode就是我想要的
        - 可以在文末增加一行
        - 如果文件不存在也会自动创建文件
```
helloFile = open('hello.txt','a')
helloFile.write('Hello')
helloFile.close()
```

## 尝试一：
```
#! /usr/bin/env python3

import sys


if len(sys.argv) >1:
    diary=open('diary.txt','a')
    diary.write("\n" + content)
    
else:
    content = diary.read()
    print(content)

diary.close()

```

之前有担心不能输入中文，后来发现顺利通过。
### Question

- 如何判断是不是第一次添加日记（日记是空白），这时不用添加空行
- 发现直接调用d.py的时候，可以添加中文没问题，  
但是直接编译的话其实是会报错的，  
估计还是diary.txt里有中文的问题，  
先记录，待解决。

```
Traceback (most recent call last):
  File "/Users/Zoe/GitHub/MyPythonScripts/d.py", line 14, in <module>
    content = diary.read()
  File "/Library/Frameworks/Python.framework/Versions/3.5/lib/python3.5/encodings/ascii.py", line 26, in decode
    return codecs.ascii_decode(input, self.errors)[0]
UnicodeDecodeError: 'ascii' codec can't decode byte 0xe6 in position 1: ordinal not in range(128)
```

## 尝试二：
#### Quesiton

- 如何添加日期

#### Solution
- [Python: Get Today’s Current Date and Time](http://www.cyberciti.biz/faq/howto-get-current-date-time-in-python/)
```
import time
print(time.strftime("%Y/%m/%d"))
```

#### 代码
```
#! /usr/bin/env python3

import sys
import time

diary=open('diary.txt','a')

if len(sys.argv) >1:
    content = ' '.join(sys.argv[1:])
    diary.write("\n" + time.strftime("%Y/%m/%d")+ ' ' +content)
    
else:
    diary=open('diary.txt')
    content = diary.read()
    print(content)

diary.close()

```

## 尝试三：

- 试着发布，就会觉得readme写的好烂，今晚先跌跌撞撞这么写着吧，以后要加强
- 当要发布给别人用的时候
    - 发现不仅要考虑自己在用的Mac OS下的Python3，还要考虑python2，还要考虑Windows
    - 发现还要告诉他们将环境配置成和我类似的，比如Path，chmod这些

#### Question
- 可不可以用类似setup.py的功能，自动完成这些配置工作