---
title: IWMPSettings baseURL property
description: The baseURL property gets or sets the base URL used for relative path resolution with URL script commands that are embedded in digital media content.
ms.assetid: e136303f-ba08-434f-ad7e-9fffa66785c4
keywords:
- baseURL property Windows Media Player
- baseURL property Windows Media Player , IWMPSettings interface
- IWMPSettings interface Windows Media Player , baseURL property
topic_type:
- apiref
api_name:
- IWMPSettings.baseURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# IWMPSettings::baseURL property

The **baseURL** property gets or sets the base URL used for relative path resolution with URL script commands that are embedded in digital media content.

## Syntax


```CSharp
public System.String baseURL {get; set;}
```

<span codelanguage="VisualBasic"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Public Property baseURL As System.String</code></pre></td>
</tr>
</tbody>
</table>



## Property value

A **System.String** that is the base URL.

## Remarks

This property specifies the base HTTP URL that is passed as the command parameter by the **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event. The base URL is concatenated with the relative URL as follows:

1.  A trailing forward slash (/) is added to the value retrieved by the **baseURL** property.
2.  A leading period, backward slash, or forward slash character (., \\, and /) is deleted from the relative URL.
3.  The relative URL is added to the end of the base URL.
4.  All slash characters in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.

**Note**

The Windows Media Player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.

## Requirements



|                      |                                                                                                                        |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9 Series or later<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## See also

<dl> <dt>

[**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**IWMPSettings Interface (VB and C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 




