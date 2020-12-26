---
title: UiPath Level 1-Lesson 1. Introduction to UiPath
authors: 智跃人才
lang: zh-CN
comments: false
toc: true
categories:
  - Business-Competence
  - RPAExcel VBA and RPA
  - UiPath
tags:
  - UiPath Level 1教程
abbrlink: 36004
updated: 2020-07-18 18:58:58
date: 2020-08-13 18:18:58
---


1. 介绍

-   Sequences：适用于单线程的程序。

-   Flowcharts：适用于比较复杂的程序，通过多个分支连接activites。

-   State Machines：适用于非常大的项目。

2. 用户界面

-   Ribbion菜单

-   快速访问工具栏

-   全局搜索栏

-   设计器面板

-   右键菜单

-   Activities面板

-   Library面板

-   Project面板

-   Properties面板

-   Outline面板

-   Output面板：显示Log Message或Write Line活动的输出。

-   Locals面板：显示当前正在运行的活动范围内的变量，仅在运行或调试时可见。

3. 快捷键

-   Ctrl + D：将当前选中的Activity放置到Comment Out中来忽略它。

-   Ctrl + E：移出Comment Out中的Activity。

-   F7：在调试模式中运行当前的Workflow。

-   F8：为当前的Workflow检查错误。

-   F9：为当前选中的Activity标记断点。

-   Shift+F9：移除当前Workflow的所有断点。

-   F5：运行当前打开的Workflow。

-   F12：停止运行或调试中的Workflow。

-   Alt + Ctrl + F：在Activities面板中搜索。

-   自定义快捷键：用记事本打开%appdata%\\UiPath\\UiPath/keyboardmappings.xml，并修改对应值。

    -   \<Key\> \</Key\>：主要键值

    -   \<Modifiers\> \</Modifiers\>：代表特殊按键（如 Ctrl, Alt, Shift,
        Windows等）

    -   \<CommandName\> \</CommandName\>：目标命令

4. 关于自动化项目

项目将保存在%userprofile%\\documents\\uipath目录中。

5. 关于自动化调试

-   日志记录：Output面板中显示有关情况的详细信息。

-   断点：在某个固定点暂停项目的执行，以检查状态。

-   **Log Message** 活动

6. 关于Library

把常用的Workflow添加到Library(库)中，就可以在其他得Workflow里把这个Workflow从Library面板拖放到设计器面板来使用它。

-   **如何添加**：在Library面板中点击“Add
    Folder”，在文件夹对话框中选择包含要添加的Workflow的文件夹。之后可以将要添加的新的Workflow直接拖放到该文件夹中。

7. 关于Activities

https://activities.uipath.com/



<br>

<center>
<b>加入万人职场社群，为自己的职业生涯保驾护航！</b>

<br>

 <img src="https://SB-HITECH.github.io/assets/img/dingding/dingding-group-excle-rpa.jpg" width = "350" height = "380" alt="万人知识共享社区" align=center />

</center>

