---
Description: Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the Selection property.
ms.assetid: 7fe0249c-c43d-498b-9029-cf5969201d96
title: InkOverlay.SelectionResizing event
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# InkOverlay.SelectionResizing event

Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.

## Syntax


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## Parameters

<dl> <dt>

*CurSelectionRect* \[in\]
</dt> <dd>

The bounding rectangle of the selection after the **SelectionResizing** event.

> [!Note]  
> This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.

 

</dd> </dl>

## Return value

This event does not return a value.

## Remarks

This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.

## Requirements



|                                     |                                                                                                                     |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP Tablet PC Edition \[desktop apps only\]<br/>                                                       |
| Minimum supported server<br/> | None supported<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt> </dl> |
| Library<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## See also

<dl> <dt>

[**InkOverlay Class**](https://msdn.microsoft.com/en-us/library/ms698599(v=VS.85).aspx)
</dt> <dt>

[**Selection Property**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[**InkRectangle Class**](https://msdn.microsoft.com/en-us/library/ms700607(v=VS.85).aspx)
</dt> </dl>

 

 



