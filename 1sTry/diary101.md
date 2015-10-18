# 交互101 - 日记系统

## 本周整体任务概述:

- 完成一个极简交互式日记系统，需求如下：
	- 一次接收输入一行日记
	- 保存为本地文件
	- 再次运行系统时,能打印出过往的所有日记
- 时限: 0wd4~1wd3
- 发布: 发布到各自仓库的 _src/om2py0w/0wex1/ 目录中
- 指标:
	- 包含软件使用说明书: README.md
	- 能令其它学员根据说明书,运行系统,完成所有功能

## 尝试一：

-  输入“diary.py 日记内容”，将内容保存为本地文件
- 要用到import sys的sys.argv
	- if len(sys.argv) >1：（含有日记内容）
		- 输入一行文字到diary.txt
		- 如果diary.txt不存在，创建它
- 输入‘diary.py’，打印以往所有日记
	- if len(sys.argv) >1：
		- 打开diary.txt	 
		- 如果diary.txt不存在，创建它

问题：

- 如何用python创建diary.txt
- 如何用python添加文字到某一个文档