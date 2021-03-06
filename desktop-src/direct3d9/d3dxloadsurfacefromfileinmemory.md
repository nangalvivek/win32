---
Description: Loads a surface from a file in memory.
ms.assetid: 436a6151-2819-44eb-bd56-1b3777f709e5
title: D3DXLoadSurfaceFromFileInMemory function (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
---

# D3DXLoadSurfaceFromFileInMemory function

Loads a surface from a file in memory.

## Syntax


```C++
HRESULT D3DXLoadSurfaceFromFileInMemory(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          LPCVOID            pSrcData,
  _In_          UINT               SrcData,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## Parameters

<dl> <dt>

*pDestSurface* \[in\]
</dt> <dd>

Type: **[**LPDIRECT3DSURFACE9**](https://msdn.microsoft.com/library/Bb205892(v=VS.85).aspx)**

Pointer to an [**IDirect3DSurface9**](https://msdn.microsoft.com/library/Bb205892(v=VS.85).aspx) interface. Specifies the destination surface, which receives the image.

</dd> <dt>

*pDestPalette* \[in\]
</dt> <dd>

Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.

</dd> <dt>

*pDestRect* \[in\]
</dt> <dd>

Type: **const [**RECT**](https://msdn.microsoft.com/library/Dd162897(v=VS.85).aspx)\***

Pointer to a [**RECT**](https://msdn.microsoft.com/library/Dd162897(v=VS.85).aspx) structure. Specifies the destination rectangle. Set this parameter to **NULL** to specify the entire surface.

</dd> <dt>

*pSrcData* \[in\]
</dt> <dd>

Type: **[**LPCVOID**](https://msdn.microsoft.com/library/Aa383751(v=VS.85).aspx)**

Pointer to the file in memory from which to load the surface.

</dd> <dt>

*SrcData* \[in\]
</dt> <dd>

Type: **[**UINT**](https://msdn.microsoft.com/library/Aa383751(v=VS.85).aspx)**

Size of the file in memory, in bytes.

</dd> <dt>

*pSrcRect* \[in\]
</dt> <dd>

Type: **const [**RECT**](https://msdn.microsoft.com/library/Dd162897(v=VS.85).aspx)\***

Pointer to a [**RECT**](https://msdn.microsoft.com/library/Dd162897(v=VS.85).aspx) structure. Specifies the source rectangle. Set this parameter to **NULL** to specify the entire image.

</dd> <dt>

*Filter* \[in\]
</dt> <dd>

Type: **[**DWORD**](https://msdn.microsoft.com/library/Aa383751(v=VS.85).aspx)**

A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered. Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.

</dd> <dt>

*ColorKey* \[in\]
</dt> <dd>

Type: **[**D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey. This is always a 32-bit ARGB color, independent of the source image format. Alpha is significant and should usually be set to FF for opaque color keys. Thus, for opaque black, the value would be equal to 0xFF000000.

</dd> <dt>

*pSrcInfo* \[in, out\]
</dt> <dd>

Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***

Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file or **NULL**.

</dd> </dl>

## Return value

Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

If the function succeeds, the return value is D3D\_OK. If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.

## Remarks

This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga. See [**D3DXIMAGE\_FILEFORMAT**](https://msdn.microsoft.com/library/Bb172878(v=VS.85).aspx).

Writing to a non-level-zero surface will not cause the dirty rectangle to be updated. If **D3DXLoadSurfaceFromFileInMemory** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](https://msdn.microsoft.com/library/Bb205910(v=VS.85).aspx) on the surface.

## Requirements



|                    |                                                                                       |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## See also

<dl> <dt>

[Texture Functions in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 




