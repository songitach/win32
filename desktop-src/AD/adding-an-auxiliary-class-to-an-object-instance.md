---
title: Adding an Auxiliary Class to an Object Instance
description: The following code examples show how to use ADSI and LDAP to dynamically add an auxiliary class to an existing object instance.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\mbaldwin
ms.assetid: 739dd372-3bda-4d94-8daf-f71e3091cfb6
ms.prod: windows-server-dev
ms.technology: active-directory-domain-services
ms.tgt_platform: multiple
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Adding an Auxiliary Class to an Object Instance

The following code examples show how to use ADSI and LDAP to dynamically add an auxiliary class to an existing object instance. The examples assume that an auxiliary class named **vehicle** is defined in the Active Directory schema, and that the **vehicle** class has a **vin** attribute.

When you dynamically add an auxiliary class to an object instance, you must simultaneously specify values for any mandatory **mustHave** attributes in the class. The following examples show how to do this with the "vin" attribute, which is assumed to be mandatory.

The following C++ example binds to an object, and uses [**IADs.PutEx**](https://msdn.microsoft.com/library/aa746353) to append the auxiliary class to the list of classes in the object's **objectClass** property. Then the example uses [**IADs.Put**](https://msdn.microsoft.com/library/aa746352) to set the value of the **vin** attribute. Finally, it calls [**IADs.SetInfo**](https://msdn.microsoft.com/library/aa746354) to commit the changes to the directory.


```C++
LPWSTR pszAuxClass[]={L"vehicle"};
LPWSTR pszVIN[]={L"df897dsfsa-0"};
VARIANT var;

VariantInit(&amp;var);

ADsOpenObject(L"cn=johnd,cn=users,dc=fabrikam,dc=com", 
    NULL, 
    NULL, 
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,  
    (VOID**)&amp;pIADs);

ADsBuildVarArrayStr(pszAuxClass, 1, &amp;var);
pIADs->PutEx(ADS_PROPERTY_APPEND, CComBSTR("objectClass"), var);
ADsBuildVarArrayStr( pszVIN, 1, &amp;var);
pIADs->Put(CComBSTR("vin"), var);
pIADs->SetInfo();

if(pIADs)
    pIADs->Release();

VariantClear(&amp;var);
```



 

 



