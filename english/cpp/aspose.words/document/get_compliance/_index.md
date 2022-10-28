---
title: get_Compliance
second_title: Aspose.Words for C++ API Reference
description: Gets the OOXML compliance version determined from the loaded document content. Makes sense only for OOXML documents.
type: docs
weight: 196
url: /cpp/aspose.words/document/get_compliance/
---
## Document.get_Compliance method


Gets the OOXML compliance version determined from the loaded document content. Makes sense only for OOXML documents.

```cpp
Aspose::Words::Saving::OoxmlCompliance Aspose::Words::Document::get_Compliance()
```


If you created a new blank document or load non OOXML document returns the **Ecma376_2006** value.

## Examples




Shows how to read a loaded document's Open Office XML compliance version. 
```cpp
// The compliance version varies between documents created by different versions of Microsoft Word.
auto doc = MakeObject<Document>(MyDir + u"Document.doc");

ASSERT_EQ(doc->get_Compliance(), OoxmlCompliance::Ecma376_2006);

doc = MakeObject<Document>(MyDir + u"Document.docx");

ASSERT_EQ(doc->get_Compliance(), OoxmlCompliance::Iso29500_2008_Transitional);
```

