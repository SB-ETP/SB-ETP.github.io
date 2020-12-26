---
title: UiPath Level 1习题集
authors: 智跃人才
lang: zh-CN
comments: false
toc: true
categories:
  - Business-Competence
  - RPAExcel VBA and RPA
  - UiPath
tags:
  - 习题集
abbrlink: 36004
updated: 2020-07-18 18:58:58
date: 2020-08-13 18:18:58
---




第一课 UiPath简介  
单选题  
1、 How can you extract structured data from a web page?  
A、Using the Citrix Recording Wizard  
B、Using the Data Scraping Wizard (√）  
C、Using the UiExplorer tool  
2、 The easiest way to get structured data from a web page is:  
A、by using Data Scraping. (√）  
B、by using Screen Scraping.  
C、by reading its contents with the Get Text activity and then parsing the
result.  
3、 Which of the following is the IDE used to develop the UiPath workflows?  
A、Ui Explorer  
B、UiPath Orchestrator  
C、UiPath Studio (√）  
4、 What recorders are best suitable for automating virtual environments?  
A、Basic B、Citrix (√） C、Web Desktop  
5、 Can you retrieve text from a Citrix environment?  
No, you cannot. Only clicks are available inside a Citrix environment.  
Yes, using the Scrape Relative function in combination with an OCR engine. (√）  
6、 What is UiPath Explorer used for?  
A、To get detailed information in regard to UI elements (√）  
B、Writing text in textboxes  
C、Clicking different elements of a web page  
7、 What are Queues used for?  
A、Schedule when a robot should start its work  
B、Describe the activities inside a process  
C、Distribute transactional load among multiple robots (√）  
8、 What activity can you use to type text in an application’s field?  
A、Click Text B、Type Into (√） C、Get Text  
9、 Can you run multiple instances of the same process, in parallel？  
A、No.  
B、Yes, on the same robot.  
C、Yes, on different robots. (√）  
10、 Where can you see the list of activities that you can use in a workflow?  
In the Activities panel (√）  
In the Project panel  
In the Outline panel  
多选题  
1、 Which of the data types can be stored in a generic variable?  
A、Integer (√） B、Boolean (√） C、String (√）  
2、 What kind of actions can be performed in the Variables panel?  
A、Setting default values for variables (√）  
B、Adding new variables (√）  
C、Changing variable types (√）  
3、 How can we change the scope of a variable?  
A、By using the Outline panel  
B、By using the Variables panel (√）  
C、By using the Manage Variables section of the Ribbon menu (√）  
备注：选项C在2019.7版本未找到 Manage Variables 功能  
4、 The Type Into activity can receive inputs like:  
A、A static string. (√）  
B、A variable followed by the .toString method. (√）  
C、An integer variable.  
5、 The Orchestrator can:  
A、Send Start commands to multiple robots (√）  
B、Schedule robots to perform specific processes (√）  
C、Remotely control robots (√）  
6、 Getting the content of a PDF document is possible:  
A、This cannot be done by a UiPath robot.  
B、By opening the PDF and using screen scraping to get its data. (√）  
C、By using the Read PDF Text activity and providing the PDF file’s path. (√）  
7、 What web scraping capabilities can UiPath implement？  
A、Extracting text based content from a webpage(√）  
B、Extracting image content from a webpage.  
C、Extracting lists or other structured data from a webpage. (√）  
D、Extracting the content of a table from a webpage. (√）  
8、 Are you restricted to the existing activities in UiPath Studio？  
A、No, you can download more activities via the Package Manager and UiPath Go!
(√）  
B、No, you can create and use Custom Activities. (√）  
C、Yes, you are restricted to the existing activities.  
第二课 变量数据类型和控制流程  
单选题  
1、 You can insert a Sequence activity in a Flowchart activity.  
A、True (√） B、False  
2、 What is the activity designed to represent a decision inside a Sequence?  
A、 The Decision activity （备注：题目说的是Sequence，Sequence中不能使用Flow
Sequence）  
B、The Try Catch activity  
C、The If activity(√） D、The Assign activity  
3、 Can you insert a Flowchart activity in a Sequence?  
A、Yes (√） C、No  
4、 What is the best way to make a three-way decision inside a Flowchart?  
A、By using nested Decision activities  
B、By using a Switch activity  
C、By using nested If activities  
D、By using a Flow Switch activity (√）  
5、 How can you exit from a For Each activity?  
A、If activity B、Assign activity C、Terminate Workflow activity D、Break
activity (√）  
6、 Which activity can you use if you want to loop through a collection of
items?  
A、Flow Decision activity B、If activity C、For Each activity (√） D、Assign
activity  
7、 What type of argument can you define to retrieve data from an invoked
workflow?  
A、Out (√） B、In  
8、 What activity can be used to execute a workflow inside another workflow?  
A、Flowchart Assign B、Invoke Workflow File (√） C、State Machine  
9、 How can you display an Integer value, myNumber, inside a Message Box window?  
A、“My number is \$myNumber”  
B、“My number is “ + myNumber.Value  
C、“My number is ” + myNumber  
D、“My number is “ + myNumber.ToString (√）  
10、 Given two Generic variables, A with value “123” and B with value 456, what
would the Write Line output of A + B be?  
A、An exception will be thrown.  
B、123 + 456  
C、579  
D、123456(√）  
11、 When having multiple activities executing in a fixed sequential order, what
kind of workflow should you use?  
A、None of the options B、Flowchart  
C、Sequence(√） D、State machine  
多选题  
1、 When should you use the Flowchart workflow?  
When having multiple activities executed in a fixed order  
When having a process with many decision blocks (√）  
When modelling a process that has loops to previous states(√）  
2、 Which activity can you use if you want to test if a condition is true or
false?  
A、Flow Decision activity (√） B、Sequence activity C、For Each activity D、If
activity (√）  
3、 Which activities allow you to iterate through an array of strings?  
A、 While (√） B、For Each Row C、For Each (√）D、Do While (√）  
备注：while循环和do…循环区别：当第一次进入循环就不满足条件时，while循环不做，do…while执行一次。其他情况输出结果是一样的。  
4、 In which variable types can you store text?  
A、String (√）B、Generic (√） C、Integer D、Double  
5、 What type of content can you store inside a Generic type variable?  
6、 A、Text (√）B、Dates (√）C、True/False (√）D、Numbers (√）  
7、 What data types can be stored inside an array?  
A、 Boolean(√） B、Integer (√）C、String (√）D、Double(√）  
8、 Which of these are workflow types available in UiPath Studio?  
A、Sequence(√） B、Activity C、Flowchart(√）  
第三课 数据操作  
单选题  
1、 What activity can you use to get the value from a certain cell, from a
specific data table row?  
A、Get Row Item(√） B、Write Cell C、Read Cell D、Remove Data Row  
备注：C是从Excel单元格中取得值  
2、 What .Net method of the datatable object can be used to filter a table by a
condition?  
A、Filter B、Select (√） C、ToString D、Clone  
3、 If the dtNewHires datatable has 4 columns, in this order : [ID, Name, Age,
Sex] and 2 rows: [1, Daniel, 38, M] ; [2, Andra, 24, F], what is the result of
the expression dtNewHires.Rows(0)(1)?  
A、1 B、Daniel (√） C、Andra D、2  
备注：dtNewHires.Rows(0)(1)是指第一行第2列。数组索引是从0开始的  
4、 What key combination allows you to automatically create a variable from an
activity’s property field?  
A、Ctrl + A B、Ctrl + K(√） C、Ctrl + N D、Ctrl + P  
5、 What variable type can you use to efficiently store the current time inside
your workflows?  
A、Array B、DateTime(√） C、Integer D、String  
6、 How can the index integer variable be displayed inside a Message Box
activity?  
A、“Current index is: “ + index.ToString(√）  
B、“Current index is: “ + index  
C、“Current index is:
*index*”*D*、“*Currentindexis*:+*index*.*ToString*”7、*WhatactivitycanbeusedtomodifythevalueofanexistingcellinaDataTable*?*A*、*Assignactivity*(√）*B*、*AddDataColumnactivityC*、*ModifyCellactivityD*、*AddDataRowactivity*8、*WhattypeofvariablescanbeusedasoutputfortheReadCSVactivity*?*A*、*List*\&lt;*DataRow*\>*variablesB*、*DataTablevariables*(√）*C*、*Array*\&lt;*DataRow*\>*variablesD*、*StringvariablesOutputDataTableactivity*9、*WhichofthefollowingstatementsaretrueregardingtheOutputDataTableactivity*?*A*、*ReturnsthedatacontainedinaDataTableasastringinacsvformat*(√）*B*、*WritesaDataTabletoanExcelfileC*、*ReturnsaDataTableobjectD*、*WritesaDataTabletoacsvfile*10、*WhatactivitycanbeusedtoloopthrougheachrowfromaDataTable*?*A*、*IfB*、*BuildDataTableC*、*FlowDecisionD*、*ForEachRow*(√）11、*Howcanwetestifagivenaddress*(*astringvariablecalledfullAddress*)*canbefoundonaparticularstreet*(*astringvariablecalledstreetName*)?*A*、*fullAddress*.*Contains*(*streetName*)(√）*B*、*streetName*.*Contains*(*fullAddress*)*C*、*streetName*.*Has*(*fullAddresss*)*D*、*fullAddress*.*Has*(*streetName*)多选题1、*IfcurrentRowrepresentsarowfromaDataTablewithtwocolumninthisorder*:*NameandAge*,*whatexpressioncanbeusedtoobtainthevaluefromthecolumnAge*?*A*、*currentRow*(\&quot;*Age*\&quot;)(√）*B*、*currentRow*.*AgeC*、*currentRow*(2)*D*、*currentRow*(1)(√）备注：列索引从“0”开始2、*Howcanyouidentifyacolumninadatatable*?*Usingthecolumnname*(√）*UsingtherownameUsingtherowindexUsingthecolumnindex*(√）3、*WhichofthefollowingdatatypesareincludedintheCollectionscategory*?*A*、*List*(√）*B*、*Array*(√）*C*、*Dictionary*(√）*D*、*Int*324、*WhatactivitiescanbeusedtoiteratethroughanArray*?*A*、*FlowDecisionB*、*While*(√）*C*、*ForEach*(√）*D*、*ForEachRow*5、*WhichofthefollowingstatementsistrueregardingListsandArrays*?*ListitemscanbeaddedusinganAddtoCollectionactivity*.(√）*Youcanaddanynumberofelementstoanarray*.*YoucaniteratethroughaListusingaForEachloopactivity*.(√）*ArrayandListelementscanbeaccessedbyindex*.(√）第四课录制单选题1、*HowcanyoudelaytheAutomaticRecording*?*A*、*ByrightclickingB*、*ByhittingtheEscapekeyC*、*ByhittingtheF*2*key*(√）*D*、*Byclickingintherightcornerofthescreen*2、*WhattypeofcontainerwillBasicRecordinggenerate*?*A*、*ExcelApplicationScopeB*、*AttachBrowserC*、*AttachWindowD*、*Nocontainer*(√）3、*WhatrecordingwizardwouldyouusetoautomateUIinteractionsinanapplicationthatdoesnotoffersupportforselectors*?*A*、*BasicRecordingB*、*CitrixRecording*(√）*C*、*WebRecordingD*、*DesktopRecording*4、*WhatisAttachWindowusedfor*?*A*、*Specifiesthatyouareworkingwithabrowser*.*B*、*Specifiesthatyouwanttoautomateinbackground*.*C*、*SpecifiesthatyouareworkingwithaJavawindow*.*D*、*Identifyingthewindowyouareworkingwith*.(√）5、*WhenisitrecommendedtouseDesktoprecording*?*A*、*WhenyouautomateCitrixApplicationsB*、*WhenyouautomateWebpagesC*、*Whenyouautomatemorestepsinthesamewindow*(√）*D*、*Whenyouautomateonestep*6、*WhattypeofcontainerwillWebRecordinggenerate*?*A*.*AttachWindowB*、*NocontainerC*、*AttachBrowser*(√）*D*、*ExcelApplicationScope*7、*Canyoucombineautomaticrecordingwithstep*−*by*−*steprecordinginthesamerecordingsequence*?*A*、*Yes*(√）*B*、*No*8、∗∗∗*WhattypeofcontainerwillWebRecordinggenerate*?*A*、*EscapeandDoubleclickB*、*Escape*(√）*C*、*F*4*andDeleteD*、*F*12多选题1、*WhatisthedifferencebetweenDesktoprecordingandBasicrecording*?*A*、*Desktoprecordinggeneratescontainers*(√）*B*、*Basicrecordergeneratesfullselectors*(√）*C*、*BasicrecorderisusedonlyforwebpagesD*、*Desktoprecordinggeneratesfullselectors*2、∗∗∗*WhichofthefollowingstatementsregardingtheAutomaticRecorderaretrue*?*A*、*ItgeneratesTypeIntoactivities*(√）*B*、*ItgeneratesClickactivities*(√）*C*、*ItcreatesaskeletonforUIautomation*(√）*D*、*ItrecognizesdifferenttypesofUIcontrols*(√）3、*Howdoyouaddactivitiestoaworkflow*?(*Selectallthatapply*.)*A*、*UsingtheAutomaticRecorder*(√）*B*、*FromtheActivitiesPanelbydragginganddropping*(√）*C*、*FromtheStepbyStepRecordingActionpane*(√）4、*WhichactionscanyourecordusingAutomaticRecording*?*A*、*CopytextB*、*Click*(√）*C*、*ScreenScrapingD*、*TypeInto*(√）第五课高级*UI*交互单选题1、*ThemainadvantageoftheOCRmethodis*:*A*、*Itworkseveniftheapplicationisrunninginthebackground*.*B*、*Itworksoneveryapplicationevenifit*’*srunninginavirtualenvironment*.(√）*C*、*It*’*sfast*.2、*Whatisthebestmethodtoextractwhitetextwrittenonbluebackgroundinadesktopapp*?*A*、*ByusingtheGoogleOCRengineB*、*ByusingtheFullTextmethod*(√）*C*、*ByusingtheGoogleOCRenginewithInvertflagD*、*ByusingtheMicrosoftOCRengine*3、*HowcanyouextractwhitetextwrittenonbluebackgroundinCitrix*?*A*、*ByusingtheNativeMethodB*、*ByusingGetTextC*、*ByusingtheMicrosoftOCRengineinvertproperty*(√）*D*、*ByusingFullTextmethod*4、*CantherobotbeprogrammedtoignoretakinghiddeninformationwhileusingtheFullTextmethod*?*A*、*NoB*、*Yes*(√）5、*WhatwouldbethebestmethodtoretrieveresultsfrommultipleGooglepages*?*A*、*DataScraping*,*becauseitcanoperatewithstructureddataandreturnadatatable*.(√）*B*、*ScreenscrapingbyusingtheFullTextmethodbecauseitretrievestheentiretext*.*C*、*Native*,*becauseitworksinthebackground*.6、*Whatisthebestactivityforscrapingtablesfromawebpage*?*A*、*GetVisibleTextB*、*Datascrapingwizard*(√）*C*、*GetOCRText*7、*Whatisthebestactivityforscrapingtablesfromawebpage*?*A*、*FullTextB*、*NoneoftheoptionsC*、*OCR*(√）*D*、*Native*多选题1、*ThedownsidesofusingtheDefaultinputmethodare*:*A*、*Theconditionthattheapplicationmustbeactive*(√）*B*、*Theconditionthattheapplicationmustberunninginbackground*.*C*、*Lowspeed*(√）2、*ThemostimportantadvantagesoftheFullTextmethodare*:*A*、*ItworksinCitrixenvironments*.*B*、*It*′*sfast*.(√）*C*、*Itworksinthebackground*.(√）*D*、*It*′*saccurate*.（准确）(√）3、*ByusingtheFullTextscrapingmethod*,*therobotisableto*:*A*、*Gethiddeninformation*(√）*B*、*Geteditabletext*(√）*C*、*Gettheentirevisibletext*(√）*D*、*Getfontinformation*(*size*,*colour*).4、*WhatistheDataScrapingwizardfor*?*A*、*AutomatinginteractionswithwebpagesB*、*ExtractingtextfromoneUIelementC*、*Extractingcorrelateddatafromtheweborotherapplications*(√）*D*、*Extractingwholetablesfromtheweborotherapplications*(√）5、*WhatistheDataScrapingwizardfor*?*A*、*SharedClipboardB*、*Native*(√）*C*、*OCR*(√）*D*、*FullText*第六课选择器（*Selectors*）单选题1、*Howcanyouimprovethefollowingcalendarpageselectortoworkonlyfordatesin*2017?*A*、“\&lt;*htmlapp*=′*chrome*.*exe*′*title*=′*UiPath*−*Calendar*−*WeekofMay*1,2017′/\>”*B*、“\&lt;*htmlapp*=′*chrome*.*exe*′*title*=′*UiPath*−*Calendar*−*Weekof*?????,2017′/\>”*C*、“\&lt;*htmlapp*=′*chrome*.*exe*′*title*=′*UiPath*−*Calendar*−∗201?′/\>“*D*、“\&lt;*htmlapp*=′*chrome*.*exe*′*title*=′*UiPath*−*Calendar*−∗2017′/\>”(√）2、*HowlongwilltheRobottrytofindanUiElement*(*ifitisnotavailable*)*onthedesktop*?*A*、*TheRobotwillwaitforeveruntilitcanfindtheelement*.*B*、10*secondsC*、*Thevalueinmillisecondsoftheactivity*’*sTimeoutMSproperty*.(√）*D*、30*seconds*3、*WhatistheHighlightactivityusefulfor*?*A*、*Fortroubleshootingandverifyingselectors*(√）*B*、*ForremovingselectorsC*、*ForaddingactivitiesinStudio*4、*HowcanyouseethefulllistofattributesofUielements*?*A*、*ByusingtheselectfromscreentoolinUiAutomationactivities*.*B*、*ByusingtheUiExplorertool*.(√）*C*、*Youcannot*.5、*CanUiExplorerbeusedtorecordUIinteractions*?*A*、*No*(√）*B*、*Yes*6、*TheElementExistsactivitythrowsanexceptionifitdoesn*’*tfindthespecifiedelementonthescreen*.*A*、*TrueB*、*False*(√）7、*Canavalidselectoridentifydifferentelementsonthescreenatthesametime*?*A*、*No*(√）*B*、*Yes*8、*Canfullselectorsbeusedinsideacontainer*(*AttachWindoworOpenApplicationactivities*)?*A*、*NoB*、*Yes*(√）9、*Canpartialselectorsbeusedinsideacontainer*(*AttachWindoworOpenApplicationactivities*)?*A*、*NoB*、*Yes*(√）10、*CanyoustoreaSelectorinavariable*?*A*、*Yes*,*oftypeString*(√）*B*、*Yes*,*oftypeInt*32*C*、*NoD*、*Yes*,*oftypeUiElement*多选题1、*WhatarethesupportedwildcardcharactersforselectorsinUiPathStudio*?*A*、

index”D、“Currentindexis:+index.ToString”7、WhatactivitycanbeusedtomodifythevalueofanexistingcellinaDataTable?A、Assignactivity(√）B、AddDataColumnactivityC、ModifyCellactivityD、AddDataRowactivity8、WhattypeofvariablescanbeusedasoutputfortheReadCSVactivity?A、List\<DataRow\>variablesB、DataTablevariables(√）C、Array\<DataRow\>variablesD、StringvariablesOutputDataTableactivity9、WhichofthefollowingstatementsaretrueregardingtheOutputDataTableactivity?A、ReturnsthedatacontainedinaDataTableasastringinacsvformat(√）B、WritesaDataTabletoanExcelfileC、ReturnsaDataTableobjectD、WritesaDataTabletoacsvfile10、WhatactivitycanbeusedtoloopthrougheachrowfromaDataTable?A、IfB、BuildDataTableC、FlowDecisionD、ForEachRow(√）11、Howcanwetestifagivenaddress(astringvariablecalledfullAddress)canbefoundonaparticularstreet(astringvariablecalledstreetName)?A、fullAddress.Contains(streetName)(√）B、streetName.Contains(fullAddress)C、streetName.Has(fullAddresss)D、fullAddress.Has(streetName)多选题1、IfcurrentRowrepresentsarowfromaDataTablewithtwocolumninthisorder:NameandAge,whatexpressioncanbeusedtoobtainthevaluefromthecolumnAge?A、currentRow("Age")(√）B、currentRow.AgeC、currentRow(2)D、currentRow(1)(√）备注：列索引从“0”开始2、Howcanyouidentifyacolumninadatatable?Usingthecolumnname(√）UsingtherownameUsingtherowindexUsingthecolumnindex(√）3、WhichofthefollowingdatatypesareincludedintheCollectionscategory?A、List(√）B、Array(√）C、Dictionary(√）D、Int324、WhatactivitiescanbeusedtoiteratethroughanArray?A、FlowDecisionB、While(√）C、ForEach(√）D、ForEachRow5、WhichofthefollowingstatementsistrueregardingListsandArrays?ListitemscanbeaddedusinganAddtoCollectionactivity.(√）Youcanaddanynumberofelementstoanarray.YoucaniteratethroughaListusingaForEachloopactivity.(√）ArrayandListelementscanbeaccessedbyindex.(√）第四课录制单选题1、HowcanyoudelaytheAutomaticRecording?A、ByrightclickingB、ByhittingtheEscapekeyC、ByhittingtheF2key(√）D、Byclickingintherightcornerofthescreen2、WhattypeofcontainerwillBasicRecordinggenerate?A、ExcelApplicationScopeB、AttachBrowserC、AttachWindowD、Nocontainer(√）3、WhatrecordingwizardwouldyouusetoautomateUIinteractionsinanapplicationthatdoesnotoffersupportforselectors?A、BasicRecordingB、CitrixRecording(√）C、WebRecordingD、DesktopRecording4、WhatisAttachWindowusedfor?A、Specifiesthatyouareworkingwithabrowser.B、Specifiesthatyouwanttoautomateinbackground.C、SpecifiesthatyouareworkingwithaJavawindow.D、Identifyingthewindowyouareworkingwith.(√）5、WhenisitrecommendedtouseDesktoprecording?A、WhenyouautomateCitrixApplicationsB、WhenyouautomateWebpagesC、Whenyouautomatemorestepsinthesamewindow(√）D、Whenyouautomateonestep6、WhattypeofcontainerwillWebRecordinggenerate?A.AttachWindowB、NocontainerC、AttachBrowser(√）D、ExcelApplicationScope7、Canyoucombineautomaticrecordingwithstep−by−steprecordinginthesamerecordingsequence?A、Yes(√）B、No8、∗∗∗WhattypeofcontainerwillWebRecordinggenerate?A、EscapeandDoubleclickB、Escape(√）C、F4andDeleteD、F12多选题1、WhatisthedifferencebetweenDesktoprecordingandBasicrecording?A、Desktoprecordinggeneratescontainers(√）B、Basicrecordergeneratesfullselectors(√）C、BasicrecorderisusedonlyforwebpagesD、Desktoprecordinggeneratesfullselectors2、∗∗∗WhichofthefollowingstatementsregardingtheAutomaticRecorderaretrue?A、ItgeneratesTypeIntoactivities(√）B、ItgeneratesClickactivities(√）C、ItcreatesaskeletonforUIautomation(√）D、ItrecognizesdifferenttypesofUIcontrols(√）3、Howdoyouaddactivitiestoaworkflow?(Selectallthatapply.)A、UsingtheAutomaticRecorder(√）B、FromtheActivitiesPanelbydragginganddropping(√）C、FromtheStepbyStepRecordingActionpane(√）4、WhichactionscanyourecordusingAutomaticRecording?A、CopytextB、Click(√）C、ScreenScrapingD、TypeInto(√）第五课高级UI交互单选题1、ThemainadvantageoftheOCRmethodis:A、Itworkseveniftheapplicationisrunninginthebackground.B、Itworksoneveryapplicationevenifit’srunninginavirtualenvironment.(√）C、It’sfast.2、Whatisthebestmethodtoextractwhitetextwrittenonbluebackgroundinadesktopapp?A、ByusingtheGoogleOCRengineB、ByusingtheFullTextmethod(√）C、ByusingtheGoogleOCRenginewithInvertflagD、ByusingtheMicrosoftOCRengine3、HowcanyouextractwhitetextwrittenonbluebackgroundinCitrix?A、ByusingtheNativeMethodB、ByusingGetTextC、ByusingtheMicrosoftOCRengineinvertproperty(√）D、ByusingFullTextmethod4、CantherobotbeprogrammedtoignoretakinghiddeninformationwhileusingtheFullTextmethod?A、NoB、Yes(√）5、WhatwouldbethebestmethodtoretrieveresultsfrommultipleGooglepages?A、DataScraping,becauseitcanoperatewithstructureddataandreturnadatatable.(√）B、ScreenscrapingbyusingtheFullTextmethodbecauseitretrievestheentiretext.C、Native,becauseitworksinthebackground.6、Whatisthebestactivityforscrapingtablesfromawebpage?A、GetVisibleTextB、Datascrapingwizard(√）C、GetOCRText7、Whatisthebestactivityforscrapingtablesfromawebpage?A、FullTextB、NoneoftheoptionsC、OCR(√）D、Native多选题1、ThedownsidesofusingtheDefaultinputmethodare:A、Theconditionthattheapplicationmustbeactive(√）B、Theconditionthattheapplicationmustberunninginbackground.C、Lowspeed(√）2、ThemostimportantadvantagesoftheFullTextmethodare:A、ItworksinCitrixenvironments.B、It′sfast.(√）C、Itworksinthebackground.(√）D、It′saccurate.（准确）(√）3、ByusingtheFullTextscrapingmethod,therobotisableto:A、Gethiddeninformation(√）B、Geteditabletext(√）C、Gettheentirevisibletext(√）D、Getfontinformation(size,colour).4、WhatistheDataScrapingwizardfor?A、AutomatinginteractionswithwebpagesB、ExtractingtextfromoneUIelementC、Extractingcorrelateddatafromtheweborotherapplications(√）D、Extractingwholetablesfromtheweborotherapplications(√）5、WhatistheDataScrapingwizardfor?A、SharedClipboardB、Native(√）C、OCR(√）D、FullText第六课选择器（Selectors）单选题1、Howcanyouimprovethefollowingcalendarpageselectortoworkonlyfordatesin2017?A、“\<htmlapp=′chrome.exe′title=′UiPath−Calendar−WeekofMay1,2017′/\>”B、“\<htmlapp=′chrome.exe′title=′UiPath−Calendar−Weekof?????,2017′/\>”C、“\<htmlapp=′chrome.exe′title=′UiPath−Calendar−∗201?′/\>“D、“\<htmlapp=′chrome.exe′title=′UiPath−Calendar−∗2017′/\>”(√）2、HowlongwilltheRobottrytofindanUiElement(ifitisnotavailable)onthedesktop?A、TheRobotwillwaitforeveruntilitcanfindtheelement.B、10secondsC、Thevalueinmillisecondsoftheactivity’sTimeoutMSproperty.(√）D、30seconds3、WhatistheHighlightactivityusefulfor?A、Fortroubleshootingandverifyingselectors(√）B、ForremovingselectorsC、ForaddingactivitiesinStudio4、HowcanyouseethefulllistofattributesofUielements?A、ByusingtheselectfromscreentoolinUiAutomationactivities.B、ByusingtheUiExplorertool.(√）C、Youcannot.5、CanUiExplorerbeusedtorecordUIinteractions?A、No(√）B、Yes6、TheElementExistsactivitythrowsanexceptionifitdoesn’tfindthespecifiedelementonthescreen.A、TrueB、False(√）7、Canavalidselectoridentifydifferentelementsonthescreenatthesametime?A、No(√）B、Yes8、Canfullselectorsbeusedinsideacontainer(AttachWindoworOpenApplicationactivities)?A、NoB、Yes(√）9、Canpartialselectorsbeusedinsideacontainer(AttachWindoworOpenApplicationactivities)?A、NoB、Yes(√）10、CanyoustoreaSelectorinavariable?A、Yes,oftypeString(√）B、Yes,oftypeInt32C、NoD、Yes,oftypeUiElement多选题1、WhatarethesupportedwildcardcharactersforselectorsinUiPathStudio?A、
B、& C、\* (√） D、? (√）  
2、 How can you improve a selector?(Select all that apply.)?  
A、By picking only the stable attributes, if possible(√）  
B、By adding attributes with dynamic values  
C、By replacing variable attribute parts with \*(√）  
D、By making sure you have an idx attribute  
3、 What is UiExplorer used for? (Select all that apply.)  
A、To explore the UI tree (√）  
B、To explore the workflow tree  
C、To create and fine tune selectors (√）  
D、UiExplorer is not a component of UiPath  
4、 Which of the following are valid options for the “nav” tag?  
A、“Prev” (√） B、“Next” (√） C、“Up” (√）  
5、 Which of the following statements are true regarding the Find Element
activity?  
A、It throws an exception if it doesn’t find the element on screen(√）  
B、It returns a boolean (True or False) values indicating wether or not the
element was found on the screen 备注：Find Element 返回的是 element  
C、It returns the found element in a variable for later use(√）  
6、 What can we use to build reliable automations when the selectors might not
be very stable?  
A、Partial selectors  
B、Anchor Base activity(√）  
C、Relative selectors(√）

第七课 图像和文本自动化  
单选题  
1、 How can you scrape a field on a Citrix Environment when the value in that
field changes each transaction?  
A、Find a static element nearby and use Scrape Relative(√）  
B、It’s impossible because you cannot locate the element  
2、 You can use image/text automation outside of a Citrix environment.?  
A、False B、True(√） 备注注意关键字 outside 虚拟环境之外当然可以  
3、 Click Image and Click OCR Text are not 100% reliable in Citrx environments.
What method can be used instead (when applicable) to have safer actions?  
A、Using full selectors.  
B、Setting the Accuracy property of the Click Image activity to 1.  
C、Setting focus on a reliable element and then navigating around the app using
keyboard (up/down arrows, tab, etc) or using keyboard shortcuts. (√）  
4、 Consider having an application in Citrix Environment that has a button named
‘Accept’ and also a label that contains the Accept word. How can Click Text be
customized in order to access the correct button?  
A、By using the Occurrence property. (√） 备注：这个属性表示第几次出现  
B、By checking the element’s attributes.  
C、It can’t be done, having to click on a text that is duplicated can’t be
controlled.  
5、 Can the robot perform clicks alongside key modifiers (Shift, Ctrl etc) in a
Citrix environment?  
A、Yes (√） B、No  
6、 By using Citrix Recorder, can you automatically record a set of actions in a
virtual environment?  
A、Yes B、No(√）  
7、 How can you improve accuracy when scraping with OCR a region that contains
only digits?  
A、Use Google OCR with “Numbers Only” (√）  
B、Use Get Text for the field in the Citrix Window  
C、Make sure the background is dark  
8、 What does the “Accuracy” property describes in “Click Image” Activity?  
A、Percent unit (0, 100] of the minimum similarity between the image found and
the image you are searching for  
B、“Click Image” does not have such a property  
C、Minimum Similarities in [0…1] percentage units for an image to be returned as
a match(√）  
9、 What method would be more reliable when clicking on a specific text label in
an application running in a Citrix environment, given the fact that its font
size might be easily changed?  
A、Using the Click Image activity.  
B、It can’t be done if its size fluctuates.  
C、Using the Click OCR Text activity. (√）  
10、 Is Reset Clipping Region mandatory to be executed at the end of a scrape
relative sequence?  
A、Yes, because Clipping Region is a shared resource. (√）  
B、No, for the next actions we can use other Clipping Regions.  
11、 What is the best way to scrape a selectable text in a Citrix environment?  
A、Use “Get Full Text” activity  
B、Use Microsoft OCR engine  
C、Select the entire text and Copy(√）  
D、Use Google OCR engine  
12、 Is it possible to click a button with Click Image Activity if the target is
not visible on the screen?  
A、No, you could click a button which is not visible only using selectors(√）  
B、Yes, the robot can click an image even if it’s not visible on the screen  
C、Yes, but you have to click the text from the button not the button image  
多选题  
1、 Creating automation in a Citrix environment is challenging because:  
A、You need to interact with the app using only Image Recognition and OCR. (√）  
B、Selectors are hard to create for virtual environments.  
C、You don’t have direct access to UI elements. (√）  
2、 Having an app in a Citrix environment with multiple text-boxes that look the
same (size/style), how can you identify one of them to type into?  
A、By using partial selectors.  
B、You can’t identify it if it doesn’t have something unique next to it
(text/image). (√）  
C、By using text-box element attributes.  
D、By clicking relative to an unique text/image next to the textbox. (√）  
3、 What activities can be used to interact with applications in a Citrix
environment?  
A、Type into(√）  
B、Click Text  
C、Click OCR Text(√）  
D、Click Image(√）  
第八课 高级Citrix自动化  
单选题  
1、 How can we make sure that an app is in a certain state in a Citrix
environment?  
A、By making use of the WaitForReady property.  
B、By checking the UI element’s attributes.  
C、By waiting for certain UI elements to appear or disappear and making
decisions based on that.(√）  
2、 \*\*\*\*How can the robot pass a variable argument when opening an
application in Citrix (eg: a web address for a browser)?  
A、 With an Open Application activity  
B、 Setting the argument to the shortcut on the desktop  
C、In the command prompt, type in the path to the application and the
argument(√）  
D、Cannot be done  
3、 Can a Pick Branch activity be used alone?  
A、No, it can only be added inside a Pick activity body. (√）  
B、Yes, for example, inside a Then/Else section of an If activity.  
4、 \*\*\*If a Click Image activity was created with an image of an icon, and
meanwhile that icon becomes highlighted, will the activity still work?  
A、No, if the accuracy is too high. (√）  
B、Yes, the robot will always find it.  
C、Yes, if the clipping region avoids the background of the icon.  
5、 What is the EASIEST navigation method to be used in a form within Citrix?  
A、By sending keyboard commands/hotkeys (√）  
B、By using Click relative to image  
C、By using Click with fixed coordinates  
6、 What happens if Find Image doesn’t actually find the desired image?  
A、An exception is thrown. (√）  
B、The output of the action will be a null object and the flow will carry on.  
7、 \*\*\*What can be done when the Windows Remote Connection doesn’t allow
sending hotkeys?  
A、There’s nothing that can be done.  
B、It should work if the Windows Remote Connection is in ‘full-screen’ mode.
(√）  
C、Send hotkeys after performing a click on the remote desktop window.  
8、 \*\*\*\*Imagine you have to use a Type Into activity in an element that
loads slowly. Will it be a good idea to add some delays before executing Type
Into?  
A、Yes, it’ll give the robot some time and when the element is loaded it can
carry on typing.  
B、No, this solution is not reliable because sometimes the loading time can take
more than the delay time.  
C、Yes, use On image appear and start typing only after the trigger happens.
(√）  
多选题  
1、 Which of the following activities can be used to select an item in drop down
list, in Citrix?  
A、Click OCR Text (√） B、Click Image (√） C、Click Text D、Select Item  
2、 How can you start an application within a Citrix environment?  
A、Using a Open Application activity  
B、Using a Start Process activity  
C、Defining a shortcut key and then triggering the app with a Send Hotkey
activity (√）  
D、Double clicking the application icon on the desktop (√）  
第九课 Excel和数据表  
单选题  
1、 What happens if you use the Excel Read Range activity to read a .xlsx file
that is already opened?  
A、It will read an empty document.  
B、It will read the document successfully. (√）  
C、It will throw an error.  
2、 What is the Output Data Table activity used for?  
A、None of the options.  
B、Printing the Data Table in the Output panel.  
C、Saves all data from the Data Table to a string variable. (√）  
D、Converting data to a Data Table.（×）  
3、 \*\*\*Can Excel related activities be used without having the Excel
Application installed?  
A、No, UiPath Studio requires MS Office package（×）  
B、Yes and it works for every Excel file（×）  
C、Yes, but only for xlsx files(√）  
D、Yes, but only for xls files（×）  
4、 \*\*You have an Excel table with two columns named “PersonName” and “Age”.
What happens if you use the activity Insert Column with the Column Name property
set to “Age”?  
A、A new column with the name “Age” is added at the beginning of the table  
B、The Column “Age” is overwritten.  
C、An exception is thrown (√）  
D、A new column with the name “Age” is added at the end of the table  
5、 What should you use if you want to get the value of a specific cell from a
row in a datatable?  
A、Add Data Row B、Output Data Table  
C、Lookup data table (√） D、Get Data Row（×）  
6、 What happens if the AddHeaders option is checked for Read Range Activity?  
A、The first row from the specified range is considered to be the column
names(√）  
B、An exception is thrown  
C、A new row is added to the excel sheet Nothing happens  
7、 What activity should you use to read all the data from a .xlsx file?  
A、Workbook Read Cell  
B、Excel Read Range (√）  
C、Workbook Read Range  
D、Excel Read Cell  
8、 You need to read from an Excel sheet and you don’t know the range. What do
you write in the “Range” property of the Read Range Activity?  
A、Write just the end cell  
B、Write an empty string (√）  
C、It’s impossible, you have to specify the range  
D、Write some random range  
9、 What activity can be used to read an entire sheet from a excel file?  
A、Write CSV B、Read Range(√） C、Get Table Range D、Read Cell  
10、 What activity can you use to create a DataTable from an input string?  
A、Generate Data Table(√） B、Output Data Table C、Build Data Table  
11、 What activity you should use if you want to calculate a sum into a cell
using Excel formulas?  
A、Excel Write Cell (√） B、Workbook Write Cell C、Excel Write Range D、Workbook
Write Range  
12、 What happens if you try to use a Write Range activity to a .xlsx file that
does not exist?  
A、It will create that file for you and write the data in it. (√）  
B、It will continue the execution without writing the data.  
C、It will throw an error.  
13、 If you need to sort a table from an .xlsx file, what should you use?  
A、An Excel Get Table Range activity.  
B、You cannot sort a table.  
C、An Excel Sort data table activity. (√）  
D、A Workbook Sort Table activity.  
14、 In order to loop through all the rows of a datatable, which activity should
be used?  
A、For Each Row (√） B、Do While C、While D、For Each  
多选题  
1、 How do you specify the Excel file to read from, in a Read Cell activity?  
A、You have to manually open the workbook  
B、In the WorkbookPath property, provide a relative path, if the workbook is in
the project folder (√）  
C、In the WorkbookPath property, provide the full path of the workbook (√）  
2、 What activity should you use if you want to add data to an existing .xlsx
document?  
A、Excel Write Cell  
B、Workbook Append Range (√）  
C、Workbook Write Range  
D、Excel Append Range (√）  
第十课 PDF  
单选题  
1、 How can a robot read only the first page of a PDF file, using the PDF
activities?  
A、Set the Range property to: 1  
B、Set the Range property to: “all”  
C、Set the Range property to: “1” (√） 备注：输入范围 是字符串类型  
2、 Will the Read PDF with OCR activity open the PDF document on the screen in
order to read it?  
A、Yes B、No(√）  
3、 If the PDF contains both images and native text, what activity should you
use to read all the text from it?  
A、Read PDF Text B、Read Image C、Read PDF with OCR(√） D、Get Text  
4、 Which of the following activities requires the PDF file to be opened with
Acrobat Reader in order to read it?  
A、Read Image B、Read PDF Text C、Get Text (√） D、Read PDF with OCR  
5、 \*\*\*If you want to extract specific information from multiple native PDF
files with the same structure, what activity should you use?  
A、Get Text (√） B、Read PDF with OCR  
C、There is no activity for this D、Get Text with OCR  
6、 If you want to extract specific information from a series of PDF files with
a similar structure but the workflow only works for one file of the series, what
should you investigate?  
A、The ContinueOnError property.  
B、None of the options  
C、The TimeoutMS property.  
D、The Selector property. (√）  
7、 If the PDF activities are not listed in your Activities Panel, how can you
get them?  
A、By going to the Output panel.  
B、By finding them in the Library tab.  
C、By installing them using the Manage Packages feature.Single choice(√）  
8、 What is the easiest way to get the invoice number from a native PDF file?  
A、Use Read PDF Text and get the value using string manipulation  
B、Use Read PDF with OCR and get the value using string manipulation  
C、Open the PDF with Acrobat and scrape only relevant information (√）  
多选题  
1、 The Read PDF with OCR activity will throw an error if the following is not
specified:  
A、The Text property. (√） B、The FileName property.(√）  
C、The Password property. D、The OCR Engine that is to be used.(√）  
2、 Which of the following statements regarding the Read PDF with OCR activity
are true?  
A、It can use different OCR engines (Microsoft, Google) (√）  
B、It works with native .pdf files (√）  
C、None of the options  
D、It allows you to specify the range of pages to be read (√）  
3、 Which of the following methods can be used for reading text from a native
.pdf document?  
A、Read PDF Text activity (√）  
B、Ui Automation (open .pdf document in Adobe Acrobat Reader, then Get Text)
(√）  
C、Read PDF with OCR activity (√）  
4、 How can you specify the location of a PDF file?  
A、 As a full path to the PDF (√） B、As a relative path (√） C、As a path to
the workflow  
5、 What activity should you use to extract all the text from the PDF file？  
A、Read PDF Text (√） B、Read PDF with OCR(√） C、Read Image D、Get Text  
6、 We have a native PDF invoice and we need to read the amount in USD next to
the label AMOUNT. What methods can we apply to get the desired value?  
A. Open the file in Acrobat Reader or any other compatible PDF reader and use
Anchor Base with the label as an anchor (√）  
B. Use a Read PDF Text activity and then use the required String manipulation
methods to retrieve only the amount (√）  
C. Use the Get Text activity with a reliable selector (if available) in order to
only retrieve the amount from the PDF file (√）  
第十一课 E-mail 自动化  
单选题  
1、 Which of the following properties are found in the Get Outlook Mail Messages
activity?  
A、Password B、Port C、Server D、MailFolder (√）  
2、 The Send Outlook Mail Message activity will work without having Microsoft
Outlook installed:  
A、False (√） B、True  
3、 What activity can you use to send an email without entering the username and
password of the email account?  
A、Send Exchange Mail Message  
B、Send Outlook Mail Message (√）  
C、Send SMTP Mail Message  
4、 What is the output of the Save Mail Message activity?  
A、None of the options.  
B、It saves a .eml file.(√）  
C、It saves a .pst file.  
D、It saves a .msg file.  
5、 Will The Get Outlook Mail Message activity delete the emails from the
account after it reads them?  
A、Yes B、No (√）  
6、 If you want to get only filtered MailMessage variables, what activity should
you use?  
A、Get Exchange Mail Messages  
B、Get POP3 Mail Messages  
C、Get IMAP mail messages  
D、Get Outlook mail messages (√）  
7、 If you are using the For Each activity to loop through a list of MailMessage
variables, what should you set the TypeArgument property to?  
A、System.Web.Mail.MailMessage  
B、System.Net.Mail.MailMessage (√）  
C、send an email message  
8、 What is the supported variable type in the Output property field of all Get
Mail activities (POP3, IMAP, Outlook, Exchange)?  
A、List (Generic) B、Generic C、MailMessage D、List (MailMessage) (√）  
9、 Which Visual Basic property within the MailMessage class will you use to get
the Date of an email?  
A、Date B、the Date cannot be retrieved  
C、Headers(“Date”) (√） D、Attachments  
多选题  
1、 What activities can you use to send an email message?  
A、Send IMAP Mail Message. 备注：IMAp没有发送邮件活动  
B、Send Outlook Mail Message. (√）  
C、Send SMTP Mail Message. (√）  
2、 How can you send an image inside a MailMessage?  
A、You can specify the relative path of the image in the Attachments property.
(√）  
B、Using an Invoke Method which allows you to Add the path to the Attachments
collection of a MailMessage object  
C、You can add the path to the attachment directly in the send activity. (√）  
D、You cannot send an image attachment inside a MailMessage.  
3、 The Save Attachments activity can save all the attachments of an email to:  
A、An absolute path. (√）  
B、In a variable, as a collection of attachment objects.  
C、A relative path. (√）  
4、 Which of the following activities will allow you to only retrieve only
unread messages? (Select all that apply.)  
A、Save Mail Message B、Get OUTLOOK Mail Message (√）  
C、Get IMAP Mail Messages (√） D、Get POP3 Mail Messages  
第十二课 调试和异常处理  
单选题  
1、 The Finally block of a Try/Catch activity is executed when:  
A、The activities in the Catch block are executed and had errors.  
B、The activities in the Try block are executed and had errors.  
C、Every time, regardless if an exception occurred or not.(√）  
D、The activities in the Try block are executed with no error.  
2、 What can you use to make sure that the execution continues even if an
activity fails?  
A、DelayAfter property B、Throw activity  
C、Try/Catch activity (√） D、TimeoutMS property  
3、 How many Catches can you have in a Try/Catch block?  
A、1 B、2 C、There is no limit on the number of catches. (√） D、5  
4、 What is the most effective way to handle the click on a UI Element that is
not always available?  
A、By using an Element Exists activity and then a Click activity.  
B、By placing the Click activity inside a Try/Catch block. (√）  
C、By setting the ContinueOnError property of the Click activity to True.  
5、 What happens if you put a Breakpoint on a Click activity and start the
workflow in Debug mode?  
A、The workflow will be paused until you click the Continue button. (√）  
B、The workflow will throw an error when it reaches that activity.  
C、The workflow will be paused for 5 seconds when it reaches that activity.  
D、You can only put a Breakpoint on a Break activity.  
6、 If you need to stop the workflow until a UI Element has disappeared from the
screen, what activity should you use?  
A、Element Exists B、Find Relative Element C、Wait Element Vanish (√） D、Find
Element  
7、 If you need to know if a UI Element is available on the screen or not, what
activity should you use?  
A、Find Element B、Element Exists (√） C、Wait Element Vanish  
8、 What does the Locals panel display when you are working in Debug mode?  
A、All the activities inside the workflow.  
B、There is no Locals panel.  
C、The current values of your variables. (√）  
D、The logs of the workflow.  
9、 When you have more than one exception type defined in the Catch block, which
block is executed?  
A、The block with most specific match (√）  
B、The block with most generic match  
C、All matching blocks in the order they are defined  
D、The first match defined  
10、 What activity can be used in a Citrix environment to check whether a UI
element is displayed or not?  
A、Image Exists(√）备注：此处题干是虚拟环境，所以不能使用C  
B、Wait Element Vanish  
C、Element Exists  
D、Find Element  
多选题  
1、 When running a workflow how can you see the steps the workflow is executing?  
A、Using Debug and inspecting the Output panel (√）  
B、Using Debug with Highlight Activities option (√）  
C、Using Run and inspecting the Properties panel  
2、 How can you run the process slower in order to analyze the robot’s behavior
in certain conditions?  
A、By using Slow Step and starting the workflow normally.  
B、By using Validate.  
C、By using Slow Step and running the workflow in Debug mode. (√）  
D、By setting up Breakpoints and running the workflow in Debug mode.  
备注：本题只有一个答案，很容易会误选D  
3、 How can execution be paused before a particular activity?  
A、By using a Break activity  
B、By using a breakpoint in Debug mode (√）  
C、By using a Pause activity 备注：没有个这活动  
D、By using a MessageBox activity (√）  
4、 What is recommended to have in a Catch block?  
A、Nothing  
B、An alternative to the approach that fails (√） 一个失败的方法的替代方案  
C、An Input Dialog activity  
D、A LogMessage activity (√）  
5、 Can you run the robot manually, step by step, in order to analyze the robot
behavior in certain conditions?  
A、Yes, by using Breakpoints and running the workflow normally  
B、No, you cannot do it.  
C、Yes, by using Step Into and Step Over. (√）  
D、Yes, by using Breakpoints and running the workflow in Debug mode. (√）  
6、 When running a workflow how can you see the steps the workflow is executing?  
A、Using Debug with Highlight Activities option(√）  
B、Using Debug and inspecting the Output panel(√）  
C、Using Run and inspecting the Properties panel  
第十三课 项目组织  
单选题  
1、 What is the recommended layout for sequential activities?  
A、Sequence (√） B、Decision C、Flowchart D、For each  
2、 What is the recommended layout for a sequence of UI interactions?  
A、Flowchart B、Decision C、Sequence (√）  
3、 What is the recommended layout to define business logic in a complex process
automation?  
A、Flowchart (√） B、Sequence C、For each D、Decision  
4、 How can you trigger another workflow from within your current one?  
A、By using the Open Application activity.  
B、By using the Invoke Method activity.  
C、By using the Invoke Workflow File activity. (√）  
Ｄ、You cannot trigger another workflow.  
5、 What activity is used to chain together multiple workflows in a single
automation?  
A、Open Application  
B、Sequence activity  
C、Flowchart activity  
D、Invoke Workflow File activity (√）  
6、 Which of the following is a good example of a workflow name?  
A、SAP_Process_Screen7.xaml  
B、Workflow1.xaml  
C、GetCustomerNumber.xaml (√）  
D、Workflow That Gets The Customer Number.xaml  
7、 When is it recommended to use nested If activities inside workflows?  
A、To replace Switch activities.  
B、Each time you must use a series of decisions.  
C、You should avoid using nested If activities. (√）  
8、 Is notifying the user via a Message Box activity a good way to keep track of
a workflow’s execution progress ?  
A、No (√） B、Yes  
多选题  
1、 What can you use to add more details about the process in the workflow
itself?  
A、Adding activity annotations (√） （增加批注）  
B、The Comment Out activity (注释掉)  
C、The Use Flowchart activity  
D、The Comment activity (√）(注释)  
2、 As a best practice, how should workflows use a local desktop application?  
A. By opening the application using the Click Image activity on the
application’s desktop shortcut.  
B. By checking if the corresponding process is running and if not, opening the
application by using the Open Application activity. (√）  
C. By using selectors to interact with the application. (√）  
D. By closing the application once it’s no longer needed. (√）  
3、 What is considered a best practice in large projects?  
A、Breaking a large process in smaller workflows(√）  
B、Giving descriptive names to variables and workflows(√）  
C、Encapsulating most used activities in single-activity workflows that can be
invoked from other workflows.  
D、Testing workflows independently(√）  
4、 What type of arguments can you use in a workflow?  
A、In(√）  
B、In/Out(√）  
C、Global  
D、Out(√）  
5、 How should an RPA developer address runtime exceptions in the workflows?  
A、By using Try/Catch blocks when invoking external workflow files(√）  
B、By using automatic recovery sequences inside the Catch blocks. (√）  
C、By logging any exception events(√）




<br>

<center>
<b>加入万人职场社群，为自己的职业生涯保驾护航！</b>

<br>

 <img src="https://SB-HITECH.github.io/assets/img/dingding/dingding-group-excle-rpa.jpg" width = "350" height = "380" alt="万人知识共享社区" align=center />

</center>