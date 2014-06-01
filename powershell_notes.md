title: Powershell_notes
date: 2014-06-02 07:29:59
tags:
	- PowerShell
	- Windows
	- Tricks	
categories:
---
Powershell应用技巧
====
## 概述
PowerShell可谓是一个异常强大的命令行工具，完美结合了GUI与命令行，由于基本兼容bash语法，所以学习难度很低，值得学习。

## 文件操作
### 新建文件及文件夹
在你的计算机上New-Item 是一个创建新文件和文件夹快而简单的的方法。

举个例子，架设你想在 C:/Scripts 文件夹内建立一个新的目录名为 Windows PowerShell 文件。仅仅只要使用New-Item ：

1）新文件夹的完整路径；

2）新的项目类型（其中你可以置顶使用 -type 参数与目录值）。这个命令在问题中看起来像这样：

	New-Item c:/scriptsWindows PowerShell -type directory


用同样的步骤创建一个新文件，文件夹，具体完整的路径名称。但是要输入 file。这个命令建立文件 C:/Scripts/New_file.txt ：

    New-Item c:/scripts ew_file.txt -type file

如果你输入的项目已经被建立存在了，你会得到一个错误的信息，类似这样：

	New-Item : The file 'C:/scripts ew_file.txt' already exists.

当然，你可以在包含 -force 参数的情况下来废除这个默认行为：

	New-Item c:/scripts ew_file.txt -type file -force

 如果你使用 -force 来键入现在有的 New_file.txt 文件将全部更新，为空文件。

说到全部更新，为空文件，你也可以使用 -value 参数来添加一些数据到你的新文件里。这个命令上加上一句，This is text added to the file 的同时建立一个New_file.txt ：

	New-Item c:/scripts ew_file.txt -type file -force -value "This is text added to the file"

New-Item 别名

    ni
### 文件夹移动及复制
可以使用mv，类似于bash中的用法，以后再叙。
