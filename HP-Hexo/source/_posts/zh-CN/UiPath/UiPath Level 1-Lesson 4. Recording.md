---
title: UiPath Level 1-Lesson 4. Recording
authors: 智跃人才
lang: zh-CN
comments: false
toc: true
categories:
  - Business-Competence
  - RPAExcel VBA and RPA
  - UiPath
tags:
  - 屏幕录制
abbrlink: 36004
updated: 2020-07-18 18:58:58
date: 2020-08-13 18:18:58
---

**学习大纲**

-   如何使用记录器 (recorders)添加用户界面活动

-   如何自定义

 

**1. 录制(Recording)功能**

录制功能可以在自动化项目的最初创建一个Workflow的框架。

**四种类型：**

-   **Basic**：桌面应用程序，如记事本(Notepad)。

-   **Desktop**：桌面应用程序，如记事本(Notepad)。

-   **Web**：浏览器和网页app。

-   **Citrix**：虚拟机，远程桌面和Citrix环境。

**基本操作：**

-   点击录制按钮，弹出上述四个选项，选择任一选项会弹出录制控制器，此处以Basic为例进行录制。

-   点击**Automatic Recorder**开始录制。

{% asset_img bed9fc44e1346910672e3d676eac46dc.png "录制" %}


-   录制开始后，蓝色的矩形表示UiPath识别出的元素，单击这些元素可与之互动。

-   以记事本为例，单击可编辑区域会弹出一个对话框，允许用户写入字符，选择特殊键值等。

{% asset_img 9be83ab60ab65725c34db0501f1ba5a1.png "录制" %}

-   Type Password：隐藏输入的内容。

    -   Empty Field：输入前清空当前编辑区域的内容。

-   按下**Esc键**可以使控制器弹出，单击**Save & Exit**或再按一次Esc键结束录制。

-   录制完成，生成一个**Recording
    Sequence**。可以在属性面板中**修改**录制的活动。

{% asset_img e2c3a8b074bb978d068726f247ea975f.png "录制" %}


-   录制产生的图片**不会影响程序运行**，仅为了方便阅读。可以在下拉菜单

{% asset_img 7e30abc5395fd76d6b7d5f53de86aa21.png "录制" %}


    中更改或删除这些图片。

    -   截图自动保存为.png文件并存放在项目文件夹下的“.screenshot”文件夹中。

**可录制和不可录制的信息：**

-   可录制信息

    -   鼠标左键单击按钮、复选框、下拉菜单等可点击的元素。

    -   在可编辑区域输入文字。

-   不可录制信息

    -   键盘快捷键

    -   辅助按键，如Ctrl键。

    -   鼠标右击

    -   鼠标悬停

    -   ……

**注意：更改了显示设置而没有重新启动计算机的情况下，UiPath无法正确识别元素。**

 

**2. Desktop录制**

Basic和Desktop都可以录制用户对桌面应用程序的操作。为了体现二者的区别，可以分别使用Basic和Desktop录制下面的操作：

-   单击已经打开的记事本的可编辑区域，输入"Hello World!"。

-   单击格式(Format)弹出下拉菜单，选择字体(Font)。

-   在字体对话框中选择18号字体。

录制完成后观察两个Sequence的不同：

-   Desktop将所有的操作放入了三个**Attach
    Window**活动中，三个窗口分别是记事本窗口，格式(Format)下拉菜单，和字体对话框。

-   Basic只是记录了操作流程，并没有添加**Attach Window**活动。

**总结 - Basic和Desktop的区别：**

**Basic **

-   活动独立存在于简单的Workflow里。

-   可能受到干扰。

**Desktop**

-   活动嵌套在**Attach Window**活动的内部；

-   不会出现干扰的问题；

-   更复杂的Workflow。

\*
Uipath通过应用程序的名称、窗口的标题、当前打开的文件等信息识别出正确的窗口，但有时会出现这些信息完全一样的情况，比如打开两个未保存过的记事本程序。如果使用Basic录制，程序会在顶层的记事本上运行，而且可能产生错误。如果使用Desktop录制，就可以避免这些干扰，找到录制时使用的那个记事本。

 

**3. 录制技巧**

-   输入的内容"Hello World!"可以改为变量。

-   在下拉菜单

{% asset_img 7e30abc5395fd76d6b7d5f53de86aa21.png "录制" %}


    中选择Indicate on Screen可以选择其他的元素，比如把更改字体改为更改字号。

-   **按下F2可以暂停录制3秒钟**，桌面右下角会出现倒计时，倒计时结束则恢复录制。F2在录制自动隐藏的菜单中的元素时非常实用。比如把打开字体对话框改为选择自动换行，为了不把点击格式(Format)下拉菜单这一步录制进去，可以先使用F2暂停录制。

-   **手动录制 **(Manual
    Recording)：在录制过程中按Esc键打开控制器，选择手工录制的功能；手工录制结束后，控制器会再次弹出，按Automatic
    Recorder键继续刚才的录制。

-   手工录制可以实现下列操作下列操作：

    -   快捷键

    -   特殊键

    -   右击鼠标

    -   鼠标悬停

    -   ……

    -   **从应用程序中获取文本信息** (Text → Copy Text)

    -   **查找元素和图片**

    -   **与剪贴板互动**

-   **Selector**：每一个录制下来的行动都会有一个selector，在属性面板Target组下面可以找到它。Selector帮助UiPath找到正确的元素或屏幕。因此，运行录好的程序时，如果UiPath无法找到元素或出现类似的问题，可以检查Selector属性。

{% asset_img 8767228a8e3721b3d37321bf254302b6.png "录制" %}


-   Edit Selector文本框里的是实际的Selector；Edit
    Attributes文本框里是相关的属性。

    -   **Attach to Live
        Element**：如果某个元素的值是变化的，比如图中的\$377就表示一个会发生变动的总金额，UiPath在元素改变后可能无法再找到它。此时单击**Attach
        to Live
        Element**，然后再次点击出现问题的元素，UiPath就会尝试去修复Selector。

 

**4. Web录制**

Web录制和Desktop比较相似：Desktop把所有录制的活动嵌套在几个**Attach
Window**里，而Web把录制的活动嵌套在几个**Attach
Browser**里，以避免其他浏览器页面的干扰。

**实例：**在Google
Finance上查找一支股票在最近两个开盘日的点数，显示一条消息告诉用户是上涨了还是下跌了。

\* 股票代码：TSLA，MSFT

[添加UiPath谷歌扩展功能](https://studio.uipath.com/v2017.1/docs/installing-the-chrome-extension)

**可能出现的问题：**

-   如何让UiPath自动打开浏览器：添加一个**Open
    Browser**活动，把它内部的**Do**删掉，把录制好的**Attach
    Browser**活动中的**Do**拖进来。

-   录制“后退”的时候会把当前网页的标题录进去。如果标题中包含特定的股票名称如TSLA，则查找另一支股票时会出现问题。解决方法是检查“后退”所在的Attach
    WIndow的Selector属性，取消勾选包含TSLA的Edit Attributes。

-   Get Text活动从网页上抓取的文本会保存在Generic Value型变量中(Td1,
    Td2)，但UiPath无法直接运算Td1-Td2。比较快捷的方式是在公式Td1-Td2的前面加上0+，即0+Td1-Td2。公式以数字开头，Uipath会默认后面的Generic
    Value型变量也是数字；以文本开头则默认后面的Generic Value型变量也是文本。

-   把**Close Application活动**放到Attach Window里，就可以关闭这个Attach
    Window所在的程序。

-   修改Recording Sequence时，如果怕把它弄乱了，可以先复制一份出来。

 

**5. 练习：**

　　1)
要求用户输入一段文本并询问保存文件使用的标题，在记事本中输入文本，设置字体样式为粗体16号字，另存为该文件为指定标题。

　　\*很简单的练习，在此不描述过程了。

　　2) 要求用户输入一个城市名，打开浏览器，在Google.com搜索“weather in \<city\>
”并抓取温度数据显示在message box里。

　　思路：

-   添加一个Input Dialog活动，用来输出变量city。

-   打开浏览器（推荐使用IE浏览器），导航到谷歌主页。

-   使用录制工具的Web录制，在Controller中选择Open
    Browser，点击打开的IE浏览器页面。

    -   注意不要点击到浏览器的窗口栏。

    -   录制工具会弹出提示让你确认URL。

-   在Controller中选择Type菜单中的Type，输入“weather in new york”。

-   选择Type菜单中的Send Hotkey。点击浏览器页面，在下拉菜单中选择Enter键。

-   选择Text菜单中Scrape→Screen Scraping，点击网页上的温度数值（生成**Get Full
    Text活动**）。

-   在Open Browser菜单中选择Close Browser。

-   单击Save & Exit退出录制。

-   把录制得到的所有活动都放到Open Broswer活动的Do里。

-   把刚才输入的new york修改为变量名city。

-   用Message Box活动显示Get Full Text活动输出的变量，即抓取的温度数据。

 

**\*本课使用过的新活动、方法、函数等：**

-   **Open Browser**

-   **Attach Browser**

-   **Close Application**

-   **Close Tab**

-   **Get Full Text**

-   **Send HotKey**


<br>

<center>
<b>加入万人职场社群，为自己的职业生涯保驾护航！</b>

<br>

 <img src="https://SB-HITECH.github.io/assets/img/dingding/dingding-group-excle-rpa.jpg" width = "350" height = "380" alt="万人知识共享社区" align=center />

</center>