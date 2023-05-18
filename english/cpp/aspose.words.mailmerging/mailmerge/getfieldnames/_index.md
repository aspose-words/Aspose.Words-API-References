---
title: Aspose::Words::MailMerging::MailMerge::GetFieldNames method
linktitle: GetFieldNames
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::MailMerge::GetFieldNames method. Returns a collection of mail merge field names available in the document in C++.'
type: docs
weight: 21000
url: /cpp/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge::GetFieldNames method


Returns a collection of mail merge field names available in the document.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNames()
```

## Remarks


Returns full merge field names including optional prefix. Does not eliminate duplicate field names.

A new string array is created on every call.

Includes "mustache" field names if [UseNonMergeFields](../get_usenonmergefields/) is **true**. 
## See Also

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
