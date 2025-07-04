---
title: Aspose::Words::EditableRange::get_SingleUser method
linktitle: get_SingleUser
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::EditableRange::get_SingleUser method. Returns or sets the single user for editable range in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words/editablerange/get_singleuser/
---
## EditableRange::get_SingleUser method


Returns or sets the single user for editable range.

```cpp
System::String Aspose::Words::EditableRange::get_SingleUser()
```

## Remarks


This editor can be stored in one of the following forms:

DOMAIN\Username - for users whose access shall be authenticated using the current user's domain credentials.

user@domain.com - for users whose access shall be authenticated using the user's e-mail address as credentials.

user - for users whose access shall be authenticated using the current user's machine credentials.

Single user and editor group cannot be set simultaneously for the specific editable range, if the one is set, the other will be clear. 
## See Also

* Class [EditableRange](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
