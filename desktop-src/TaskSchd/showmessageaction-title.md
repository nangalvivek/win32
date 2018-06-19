---
title: ShowMessageAction.Title property
description: For scripting, gets or sets the title of the message box.
ms.assetid: 6ec51ebb-5aa3-4338-bc88-dd8df34d59ac
keywords:
- Title property Task Scheduler
- Title property Task Scheduler , ShowMessageAction object
- ShowMessageAction object Task Scheduler , Title property
topic_type:
- apiref
api_name:
- ShowMessageAction.Title
api_location:
- taskschd.dll
api_type:
- COM
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# ShowMessageAction.Title property

\[This object is no longer supported. You can use IExecAction with the Windows scripting [**MsgBox function**](https://msdn.microsoft.com/en-US/library/sfw6660x(v=VS.80).aspx) to show a message in the user session.\]

For scripting, gets or sets the title of the message box.

## Syntax


```VB
ShowMessageAction.Title As String
```



## Property value

The title of the message box.

## Remarks

Parameterized strings can be used in the title text of the message box. For more information, see the Examples section in [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).

When setting this property value, the value can be text that is retrieved from a resource .dll file. A specialized string is used to reference the text from the resource file. The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text. For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                          |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                    |
| End of client support<br/>    | Windows 7<br/>                                                                    |
| End of server support<br/>    | Windows Server 2008 R2<br/>                                                       |
| Type library<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## See also

<dl> <dt>

[**ShowMessageAction**](showmessageaction.md)
</dt> </dl>

 

 




