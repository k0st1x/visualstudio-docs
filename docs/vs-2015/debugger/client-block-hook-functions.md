---
title: "Client Block Hook Functions | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.debug.hooks"
dev_langs: 
  - "FSharp"
  - "VB"
  - "CSharp"
  - "C++"
  - "C++"
helpviewer_keywords: 
  - "client blocks, validating and reporting data"
  - "debugging [C++], hook functions"
  - "_CrtSetDumpClient function"
  - "client blocks, hook functions"
  - "hooks, client block"
ms.assetid: f21c197e-565d-4e3f-9b27-4c018c9b87fc
caps.latest.revision: 18
author: "mikejo5000"
ms.author: "mikejo"
manager: "ghogen"
---
# Client Block Hook Functions
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

The latest version of this topic can be found at [Client Block Hook Functions](https://docs.microsoft.com/visualstudio/debugger/client-block-hook-functions).  
  
If you want to validate or report the contents of the data stored in `_CLIENT_BLOCK` blocks, you can write a function specifically for this purpose. The function that you write must have a prototype similar to the following, as defined in CRTDBG.H:  
  
```  
void YourClientDump(void *, size_t)  
  
```  
  
 In other words, your hook function should accept a **void** pointer to the beginning of the allocation block, together with a **size_t** type value indicating the size of the allocation, and return `void`. Other than that, its contents are up to you.  
  
 Once you have installed your hook function using [_CrtSetDumpClient](http://msdn.microsoft.com/library/f3dd06d0-c331-4a12-b68d-25378d112033), it will be called every time a `_CLIENT_BLOCK` block is dumped. You can then use [_CrtReportBlockType](http://msdn.microsoft.com/library/0f4b9da7-bebb-4956-9541-b2581640ec6b) to get information on the type or subtype of dumped blocks.  
  
 The pointer to your function that you pass to `_CrtSetDumpClient` is of type **_CRT_DUMP_CLIENT**, as defined in CRTDBG.H:  
  
```  
typedef void (__cdecl *_CRT_DUMP_CLIENT)  
   (void *, size_t);  
```  
  
## See Also  
 [Debug Hook Function Writing](../debugger/debug-hook-function-writing.md)   
 [crt_dbg2 Sample](http://msdn.microsoft.com/en-us/21e1346a-6a17-4f57-b275-c76813089167)   
 [_CrtReportBlockType](http://msdn.microsoft.com/library/0f4b9da7-bebb-4956-9541-b2581640ec6b)



