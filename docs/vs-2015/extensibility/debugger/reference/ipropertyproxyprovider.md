---
title: "IPropertyProxyProvider | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "IPropertyProxyProvider"
helpviewer_keywords: 
  - "IPropertyProxyProvider interface"
ms.assetid: 52e9f7fc-6fe0-4d23-890b-5673dca8c3cb
caps.latest.revision: 12
ms.author: "gregvanl"
manager: "ghogen"
---
# IPropertyProxyProvider
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

The latest version of this topic can be found at [IPropertyProxyProvider](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/ipropertyproxyprovider).  
  
This interface supplies a proxy interface to view and change an object's data.  
  
## Syntax  
  
```  
IPropertyProxyProvider : IUnknown  
```  
  
## Notes for Implementers  
 The expression evaluator (EE) implements this interface on the same object that implements the [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md) interface as part of the EE's support of type visualizers.  
  
## Notes for Callers  
 Call [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) on an `IDebugProperty3` interface to obtain this interface.  
  
## Methods in Vtable order  
 The `IPropertyProxyProvider` interface implements the following method:  
  
|Method|Description|  
|------------|-----------------|  
|[GetPropertyProxy](../../../extensibility/debugger/reference/ipropertyproxyprovider-getpropertyproxy.md)|Retrieves a property proxy interface to view data on an object.|  
  
## Remarks  
 Although the EE implements this interface, the implementation of [GetPropertyProxy](../../../extensibility/debugger/reference/ipropertyproxyprovider-getpropertyproxy.md) is typically handled by [GetPropertyProxy](../../../extensibility/debugger/reference/ieevisualizerservice-getpropertyproxy.md). See [Visualizing and Viewing Data](../../../extensibility/debugger/visualizing-and-viewing-data.md) for details on obtaining the IEEVisualizerService interface.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../../../extensibility/debugger/reference/core-interfaces.md)   
 [GetPropertyProxy](../../../extensibility/debugger/reference/ieevisualizerservice-getpropertyproxy.md)   
 [Type Visualizer and Custom Viewer](../../../extensibility/debugger/type-visualizer-and-custom-viewer.md)   
 [Visualizing and Viewing Data](../../../extensibility/debugger/visualizing-and-viewing-data.md)

