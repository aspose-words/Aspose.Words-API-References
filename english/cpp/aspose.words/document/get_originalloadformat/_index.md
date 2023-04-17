---
title: Aspose::Words::Document::get_OriginalLoadFormat method
linktitle: get_OriginalLoadFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_OriginalLoadFormat method. Gets the format of the original document that was loaded into this object in C++.'
type: docs
weight: 41000
url: /cpp/aspose.words/document/get_originalloadformat/
---
## Document::get_OriginalLoadFormat method


Gets the format of the original document that was loaded into this object.

```cpp
Aspose::Words::LoadFormat Aspose::Words::Document::get_OriginalLoadFormat() const
```

## Remarks


If you created a new blank document, returns the [Doc](../../loadformat/) value.

## Examples



Shows how to retrieve details of a document's load operation. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

ASSERT_EQ(MyDir + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(LoadFormat::Docx, doc->get_OriginalLoadFormat());
```

## See Also

* Enum [LoadFormat](../../loadformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
