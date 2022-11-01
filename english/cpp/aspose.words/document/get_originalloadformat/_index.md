---
title: get_OriginalLoadFormat
second_title: Aspose.Words for C++ API Reference
description: Gets the format of the original document that was loaded into this object.
type: docs
weight: 482
url: /cpp/aspose.words/document/get_originalloadformat/
---
## Document.get_OriginalLoadFormat method


Gets the format of the original document that was loaded into this object.

```cpp
Aspose::Words::LoadFormat Aspose::Words::Document::get_OriginalLoadFormat() const
```


If you created a new blank document, returns the **Doc** value.

## Examples




Shows how to retrieve details of a document's load operation. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

ASSERT_EQ(MyDir + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(LoadFormat::Docx, doc->get_OriginalLoadFormat());
```

