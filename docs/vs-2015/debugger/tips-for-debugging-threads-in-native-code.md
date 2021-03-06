---
title: "Tips for Debugging Threads in Native Code | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "FSharp"
  - "VB"
  - "CSharp"
  - "C++"
helpviewer_keywords: 
  - "threading [Visual Studio], debugging"
  - "debugging [Visual Studio], threads"
ms.assetid: 0374c8c6-57a3-4cfe-8047-2effef5ff5dc
caps.latest.revision: 25
author: "mikejo5000"
ms.author: "mikejo"
manager: "ghogen"
---
# Tips for Debugging Threads in Native Code
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

The latest version of this topic can be found at [Tips for Debugging Threads in Native Code](https://docs.microsoft.com/visualstudio/debugger/tips-for-debugging-threads-in-native-code).  
  
Here are some tips you can use when debugging threads in native code:  
  
-   You can view the contents of the Thread Information Block by typing `@TIB` in the **Watch** window or **QuickWatch** dialog box.  
  
-   You can view the last error code for the current thread by entering `@Err` in the **Watch** window or **QuickWatch** dialog box.  
  
-   C Run-Time Libraries (CRT) functions can be useful for debugging a multithreaded application. For more information, see [_malloc_dbg](http://msdn.microsoft.com/library/c97eca51-140b-4461-8bd2-28965b49ecdb).  
  
## See Also  
 [Debug Multithreaded Applications](../debugger/debug-multithreaded-applications-in-visual-studio.md)   
 [Debugging Native Code](../debugger/debugging-native-code.md)



