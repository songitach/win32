---
Description: Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.
ms.assetid: d4752a6c-2114-4016-a69f-dcc561d2c76b
title: ID3DXMATRIXStack::TranslateLocal method
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# ID3DXMATRIXStack::TranslateLocal method

Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.

## Syntax


```C++
HRESULT TranslateLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## Parameters

<dl> <dt>

*x* \[in\]
</dt> <dd>

Type: **[**FLOAT**](https://msdn.microsoft.com/windows/desktop/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

The translation factor in the x-direction.

</dd> <dt>

*y* \[in\]
</dt> <dd>

Type: **[**FLOAT**](https://msdn.microsoft.com/windows/desktop/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

The translation factor in the y-direction.

</dd> <dt>

*z* \[in\]
</dt> <dd>

Type: **[**FLOAT**](https://msdn.microsoft.com/windows/desktop/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

The translation factor in the z-direction.

</dd> </dl>

## Return value

Type: **[**HRESULT**](https://msdn.microsoft.com/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the method succeeds, the return value is D3D\_OK.

## Remarks

This method left-multiplies the current matrix with the computed translation matrix (transformation is about the local origin of the object).


```
    
D3DXMATRIX tmp;
D3DXMatrixTranslation( &amp;tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::Translate**](id3dxmatrixstack--translate.md)
</dt> </dl>

 

 



