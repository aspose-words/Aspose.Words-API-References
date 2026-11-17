---
title: Aspose::Words::EditableRange::set_SingleUser method
linktitle: set_SingleUser
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::EditableRange::set_SingleUser method. Sets the single user for editable range in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words/editablerange/set_singleuser/
---
## EditableRange::set_SingleUser method


Sets the single user for editable range.

```cpp
void Aspose::Words::EditableRange::set_SingleUser(const System::String & value)
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
