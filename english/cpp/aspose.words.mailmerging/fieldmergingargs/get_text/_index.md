---
title: Aspose::Words::MailMerging::FieldMergingArgs::get_Text method
linktitle: get_Text
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::FieldMergingArgs::get_Text method. Gets or sets the text that will be inserted into the document for the current merge field in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.mailmerging/fieldmergingargs/get_text/
---
## FieldMergingArgs::get_Text method


Gets or sets the text that will be inserted into the document for the current merge field.

```cpp
System::String Aspose::Words::MailMerging::FieldMergingArgs::get_Text() const
```

## Remarks


When your event handler is called, this property is set to **null**.

If you leave Text as **null**, the mail merge engine will insert [FieldValue](../../fieldmergingargsbase/get_fieldvalue/) in place of the merge field.

If you set Text to any string (including empty), the string will be inserted into the document in place of the merge field. 
## See Also

* Class [FieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
