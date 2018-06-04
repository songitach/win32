---
Description: Removes generic component settings from a virtual system configuration.
ms.assetid: 54ddb960-65b7-409d-ad80-f3685562a1a1
title: RemoveSystemComponentSettings method of the Msvm\_VirtualSystemManagementService class
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# RemoveSystemComponentSettings method of the Msvm\_VirtualSystemManagementService class

Removes generic component settings from a virtual system configuration.

## Syntax


```mof
uint32 RemoveSystemComponentSettings(
  [in]  Msvm_SystemComponentSettingData REF ComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## Parameters

<dl> <dt>

*ComponentSettings* \[in\]
</dt> <dd>

Array of [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that reference the component settings to remove.

</dd> <dt>

*Job* \[out\]
</dt> <dd>

If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](https://msdn.microsoft.com/library/cc136808).

</dd> </dl>

## Return value

Returns 0 or 4096 on a success; otherwise, returns an error.

<dl> <dt>

**Completed with No Error** (0)
</dt> <dt>

**Not Supported** (1)
</dt> <dt>

**Failed** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Invalid Parameter** (4)
</dt> <dt>

**Invalid State** (5)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Method Parameters Checked - Job Started** (4096)
</dt> <dt>

**Method Reserved** (4097..32767)
</dt> <dt>

**Vendor Specific** (32768..65535)
</dt> </dl>

## Requirements



|                                     |                                                                                                         |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 10, version 1703 \[desktop apps only\]<br/>                                               |
| Minimum supported server<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Root\\virtualization\\v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## See also

<dl> <dt>

[**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 



