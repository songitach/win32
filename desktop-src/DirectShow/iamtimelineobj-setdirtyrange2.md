---
Description: Not implemented.
ms.assetid: 14ff2979-134f-45e4-98e1-1a119e1ffee2
title: IAMTimelineObj::SetDirtyRange2 method
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# IAMTimelineObj::SetDirtyRange2 method

> [!Note]  
> \[Deprecated. This API may be removed from future releases of Windows.\]

 

Not implemented.

## Syntax


```C++
HRESULT SetDirtyRange2(
   REFTIME Start,
   REFTIME Stop
);
```



## Parameters

<dl> <dt>

*Start* 
</dt> <dd>

Reserved.

</dd> <dt>

*Stop* 
</dt> <dd>

Reserved.

</dd> </dl>

## Return value

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Remarks

> [!Note]  
> The header file Qedit.h is not compatible with Direct3D headers later than version 7.

 

> [!Note]  
> To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](http://go.microsoft.com/fwlink/p/?linkid=129787). Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.

 

## Requirements



|                    |                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Library<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## See also

<dl> <dt>

[**IAMTimelineObj Interface**](iamtimelineobj.md)
</dt> </dl>

 

 



