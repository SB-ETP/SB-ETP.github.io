---
title: UiPath Level 1-Lesson 5. Advanced UI Interaction
authors: 智跃人才
lang: zh-CN
comments: false
toc: true
categories:
  - Business-Competence
  - RPAExcel VBA and RPA
  - UiPath
tags:
  - UI交互
abbrlink: 36004
updated: 2020-07-18 18:58:58
date: 2020-08-13 18:18:58
---


**学习大纲**

-   创建Input的三种方法和它们之间的不同

-   如何使用Screen Scraping Wizard

-   创建Output的三种方法和它们之间的不同

-   如何使用Data Scraping Wizard

 

与UI的交互 (UI Interaction) 可以分为两种：Input和Output。

**Input (输入)**：使应用程序做某件事。如鼠标单击、文本录入、键盘快捷键、鼠标右击、鼠标悬停等。

**Output (输出)**：从应用程序中提取信息。获得文本，找到元素和图片，操作剪贴板等。

 

**1. Input方法**

| **Input方法**       | ** 兼容性 ** | **运行速度** | **支持后台工作** | **支持Hotkeys** | **自动清空内容** |
|---------------------|--------------|--------------|------------------|-----------------|------------------|
| Default             | 100%         | 50%          | X                | √               | X                |
| Window Messages     | 80%          | 50%          | √                | √               | X                |
| Simulate Type/Click | \*70%        | 100%         | √                | X               | √                |

 


\*Simulate Type/Click可以兼容99%的网页应用和60%的桌面应用程序

-   Default方法使用鼠标和键盘的驱动模拟人为使用。这种方法总是管用，但是运行速度慢，而且不可以在后台操作。

-   可以先使用Default方法确保程序能正常运行，然后再修改为其他两种方法，看看是否能运行。

-   如果不需要发送热键，推荐使用Simulate方法，因为它的速度最快，且支持后台运行。之后再考虑尝试Window
    Messages方法。

-   可以在属性面板里选择使用那种Input方法。

**实例验证：**

-   打开记事本，使用Basic进行录制。

-   在记事本中输入一段较长的文本A (Type Into活动1)，再输入另一段文本B (Type
    Into活动2)，最小化记事本 (Click活动)。

-   录制结束后，把Click活动拖到两个Type Into活动之间，以测试后台运行。

-   在Type Info活动2里，手动添加一个热键Enter
    (点击右下角的下拉箭头选择热键)，添加后显示为"[k(enter)]文本B"。

{% asset_img 1fdcdaeb294456ccbd852b6a46cfe8b0.png "UI交互" %}


{% asset_img 4e8c67207d82f60e052d7df832d78638.png "UI交互" %}


**运行结果：**

-   **Default：文本A（换行）文本B**  
    速度较慢；最小化窗口之后又还原窗口，再输入文本B； 识别了[k(enter)]。

-   **WindowMessages：文本a（换行）文本b**  
    速度最慢；最小化窗口后在后台输入文本B；识别了[k(enter)]；**大写字母都变成了小写**。

-   **Simulate：[k(enter)]文本B**  
    速度最快；最小化窗口后再后台输入文本B；不能识别[k(enter)]；虽然没有勾选Empty
    Filed选项，但是文本A在输入文本B时被清空了。  
    **解决方法：**在第二个Type Info活动前添加**Get
    Text**活动提取文本A，再把文本B附在文本A的后面输入。

**建议：**每一种Input方法都试一下。先使用**Default**方法，因为它是一定可以运行的。之后再尝试使用**Simulate**或**WindowMessages**方法来提高运行速度或者实现在后台工作。

 

**2. Output方法：Screen Scraping**

上一课用到的Get Text活动仅适合抓取简单短小的文本。而**Screen
Scraping**可以抓取更大块的、存在于复杂元素中的文本。Screen
Scraping还可以获取文本的位置、颜色等信息。

使用Screen Scraping工具抓取信息时可以尝试下面三种方法：

| ** Output方法 ** | **运行速度** | ** 准确度 ** | **支持后台工作** | **获取文本位置** | **获取隐藏文本** | **兼容Citrix** |
|------------------|--------------|--------------|------------------|------------------|------------------|----------------|
| FullText         | 很快         | 100%         | √                | X                | √                | X              |
| Native           | 较快         | 100%         | X                | √                | X                | X              |
| OCR              | 很慢         | 98%          | X                | √                | X                | √              |

 


1) **FullText**是默认方法，大多数情况下也有是有效的方法。

2) **Native**的优势是可以获取文字的其他信息，比如某个单词或字母在屏幕上的坐标。

3) **OCR** 不能达到100%的准确度，但当另外两种方法不起作用时，OCR就是最后手段。

　　\*只有OCR可以在Citrix或者虚拟环境下运行。OCR也可以获取文字位置。

 

**怎样使用Screen Scraping：**

　　1) 点击Design Ribbon中的Screen Scraping按钮，会出现选取界面。


{% asset_img 9b61e8aa3f32e23f7105baf2afff8abc.png "UI交互" %}

　　2) 点击以选择想要提取的信息，可以选择**包含多个元素**的区域。

{% asset_img 634458cc73e88897a8662f7fc43067a9.png "UI交互" %}

 

　　3) 选取完会弹出**Screen Scraper Wizard**窗口。点击**UI
Element**或**Region**可以更改提取信息的区域。

　　这里UiPath自动选择了**Native方法**，可以在**Options**面板中更改为其它两种方法。

{% asset_img f892743cb4c36db7e7de022f15833a9b.png "UI交互" %}


　　从预览面板中可以看出，**Native方法**只抓取了可编辑区域中的文本。

 

　　4) 切换为**Full Text方法**后，预览面板中的信息发生了变化。

　　**Full
Text方法**不但抓取了可编辑区域的文本，还抓取了不可编辑区域的文本和隐藏在下拉列表中的文本。

{% asset_img 2b234370039e26fc709d7142c1950cb7.png "UI交互" %}


　　\*在Options面板中勾选**Ignore
Hidden**选项，再点**Re-scrape**按钮可以忽略隐藏的文本。

{% asset_img 91c412c5d4fffc35ec1d1c343b26a2ff.png "UI交互" %}

 

　　5) **OCR方法**则更为不同，它把选择的区域看作图片来读取其中的文字。

　　由于会出现错别字，OCR方法仅适用于数据不需要完全正确的情况。

{% asset_img 21f141a4a176deef631a1c2b0f46f225.png "UI交互" %}


　　UiPath提供了两个OCR的引擎。**MS Office
OCR适用于较大的图片**，比如扫描的文档。


　　**Google OCR更适合读取较小的、分辨率较低的图片**，比如界面上的元素。

{% asset_img 0897e2abb71118033265e0895ac9a610.png "UI交互" %}


　　Options面板中**Invert**选项专门针对一些**黑底白字**的图片。**Scale**选项则可以放大图片以得到更好的结果。

　　我们可以逐个尝试这些选项，看看预览面板的结果有什么变化，找到最佳组合方式。

 

 　　6) 设置完点击右下角的**Continue**按钮，会得到一个ScreenScraping的Sequence。

{% asset_img 6d0fcb77ec8ebc3c4de74df37a732d90.png "UI交互" %}


{% asset_img 8005e7a53e7cbfd497a6179aa247799e.png "UI交互" %}


　　**Selector**表示要抓取文本的元素或区域，当多个活动的元素或区域相同时，可以将Selector里的内容**直接复制到其他活动中**而不必重新选择元素或区域。**Text**的变量用来保存抓取到的文本。

　　如果想试试另一种OCR，可以把**Google OCR活动**删除，再把**MS Office
OCR活动**拖进来。推荐把**Scale属性**改成3，因为MS Office
OCR更适合读取较大的图片。

 

**\*如果不使用Screen Scraping，也可以手动添加活动。**

| **Output方法**  | **手动添加**     |
|-----------------|------------------|
| Basic Recording | Get Text         |
| Full Text       | Get Full Text    |
| Native          | Get Visible Text |
| OCR             | Get OCR Text     |

 

**\***Get Text活动在上例中只能抓取"Address"一个单词。 

 

**3. Data Scraping**

Screen Scraping用来抓取**Freeform Data** (自由形式的数据)。而**Data
Scraping**用来抓取**Structured Data (结构化数据)**。

**Structured Data是什么？**  
当你在Google搜索某个关键词时，你得到的搜索结果是由很多块相同格式的数据构成的，每一块都由三部分构成：标题、URL和描述。这样的数据就是**Structured
Data**。

{% asset_img 4a6eaef6c31a7b3f190e83b17be5781e.png "UI交互" %}
 

**怎样使用Data Scraping：**

以亚马逊的图书搜索页面为例，该页面上的数据也是**Structured
Data**，但是比Google的搜索结果页面更为复杂。

{% asset_img 58f9b306543321e0128644b64a8c5d56.png "UI交互" %}
 

　　1) 点击Design Ribbon中的**Web
Scraping**按钮，会出现向导窗口，点击**Next**就可以开始选取第一个元素了。

{% asset_img 09a5f7479750edaa339a6b3e2f802f8b.png "UI交互" %}


{% asset_img da0a6228c7e996bb7b27858f78dedb82.png "UI交互" %}


　　2) 点击第一本书的标题，会再次弹出向导窗口。点击**Next**继续。


{% asset_img cc80dc163d08d6a3a9949bad7876eafd.png "UI交互" %}


{% asset_img 4e3ad6bcb3c7d2abe037068dd895f8ad.png "UI交互" %}



　　3)点击第二本书的标题，再次弹出向导窗口。图书的标题也是**链接**，因此向导窗口可以选择提取文本或URL。


{% asset_img b2fd941387cb5a27a68d540d0217a48b.png "UI交互" %}



　　这里两个选项都勾选上，分别命名为Title和URL。点击**Next**按钮，弹出向导的预览界面。

{% asset_img 030ba21800e877dc9db4ea8ee32e0cb5.png "UI交互" %}


　　4)除了提供预览的数据，网页上的相应位置被标出来方便查看。接着提取“作者”和“价格”，点击**ExtractCorrelated Data**按钮。

{% asset_img 09e4060eb7820e47b45c6e437cb353894.png "UI交互" %}


　　5)向导重新回到选择第一个元素时的界面，重复上面的步骤提取“作者”和“价格”信息。点击**Finish**按钮。  

　　6)UiPath会询问我们数据是否跨页。将网页下拉到选择页码的地方，选择**Yes**，然后选择网页上的**Next Page**元素。

{% asset_img aefda465cb923cee05f9468e24e89fcd.png "UI交互" %}

{% asset_img f8b7f42f87d7993b44697208e9d9c9b2.png "UI交互" %}

　　7) 向导结束后将得到一个名为WebScraping的Sequence，并且得到一个**DataTable**类型的Output变量。

　　    添加一个**Write CSV活动**，将抓取的数据保存在一个CSV文件里。

　　8)这个CSV文件里有100条记录，但搜索结果远超100条。这是因为UiPath默认只抓取100条记录，可以在属性面板里更改设置。

{% asset_img 8aaf60cf44e27dba215213bbea255a60.png "UI交互" %}


用Web Scraping抓取**网页上的表格 (HTML Table)** 是，当点击表格里的任意一个单元格会弹出**Extract Table提示窗口**。

如果选择**Yes**，就可以**直接抓出整个表格的数据**，而不需要选择第二个元素。如果选择**No**，则需要重复之前的步骤选择第二个元素。

{% asset_img eae824dc5bbc68cae60439523d54e603.png "UI交互" %}


**4. 练习：**

1) 提取链接页面的100条记录，包括名称和价格，将数据存储到一个新建的Excel表格中。

\*第一次选取该页的第一个名称，
第二次选取该页的最后一个名称。相比于第二次选取第二个名称，这样更有可能生成一个一致的标识符
(a consistent identifier)。

2)不适用Recording功能完成一下操作：在记事本中打开字体对话框，将字体改为Arial，样式改为斜体，增大5个字号，并选择一个新的脚本
(Script)。

-   打开记事本，添加一个**Attach Window活动**。

-   在Attach Window活动的Do里添加一个**Click活动**。点击**蓝字Indicate element
    inside window**指定元素，接着点击记事本的格式菜单 (Format) 按钮。

-   在第一个Attach Window活动之后再添加一个**Attach
    Window活动**。**按下F2暂停**并打开格式菜单，暂停结束后点击弹出的格式菜单。

    -   因为UiPath会把格式菜单当作一个新的窗口，所以需要添加一个新的Attach
        Window活动。

-   在第二个Attach Window活动的Do里添加一个**Click活动**，点击格式菜单里的字体
    (Font) 按钮。

-   为弹出的字体对话框添加一个新的**Attach Window活动**。

-   在第三个Attach Window活动的Do里添加一个**Type
    Into活动**，指定元素并点击字体的输入框，输入Arial。

-   再添加一个**Type Into活动**，指定元素并点击字体样式的输入框，输入Italic。

-   添加一个**Get
    Text活动**，指定元素并点击字号的输入框。新建一个Int32型的变量**fontSize**，将它设置为Get
    Text活动的Output。

-   添加一个**Type
    Into活动**，指定元素并点击字号的输入框，输入**(fontSize+5).ToString**。

-   添加一个**Select
    Item活动**，指定Script的下拉菜单为**Target的Selector参数**，输入Greek作为**Input的Item参数**。

**注意：**

-   F2暂停并不是只能在Recording的时候用，在选取元素的时候都可以使用。

-   如果用Ctrl+L创建的变量提示类型错误，可以尝试在变量面板重新创建。

 

**\*本课使用过的新活动、方法、函数等：**

-   **Get Full Text**

-   **Get Visible Text**

-   **Get OCR Text**

-   **Google OCR**

-   **MS Office OCR**

-   **Write CSV**

-   **Write Range**：将DataTable数据写入一个Excel表格。

-   **Click**

-   **Select Item**：选择下拉菜单可以用这个活动。

-   Environment.Newline：**添加新行。**例如："Get Full Text: " + textGFT **+
    Environment.Newline +** "Get Visible Text: " + textGVT


<br>

<center>
<b>加入万人职场社群，为自己的职业生涯保驾护航！</b>

<br>

 <img src="https://SB-HITECH.github.io/assets/img/dingding/dingding-group-excle-rpa.jpg" width = "350" height = "380" alt="万人知识共享社区" align=center />

</center>