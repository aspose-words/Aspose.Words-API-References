---
title: Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName method
linktitle: get_DocumentFieldName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName method. Gets the name of the merge field as specified in the document in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.mailmerging/fieldmergingargsbase/get_documentfieldname/
---
## FieldMergingArgsBase::get_DocumentFieldName method


Gets the name of the merge field as specified in the document.

```cpp
System::String Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName() const
```

## Remarks


If you have a mapping from a document field name to a different data source field name, then this is the original field name as specified in the document.

If you specified a field name prefix, for example "Image:MyFieldName" in the document, then [DocumentFieldName](./) returns field name without the prefix, that is "MyFieldName". 
## See Also

* Class [FieldMergingArgsBase](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
