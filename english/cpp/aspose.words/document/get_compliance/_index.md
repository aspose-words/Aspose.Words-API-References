---
title: Aspose::Words::Document::get_Compliance method
linktitle: get_Compliance
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_Compliance method. Gets the OOXML compliance version determined from the loaded document content. Makes sense only for OOXML documents in C++.'
type: docs
weight: 17000
url: /cpp/aspose.words/document/get_compliance/
---
## Document::get_Compliance method


Gets the OOXML compliance version determined from the loaded document content. Makes sense only for OOXML documents.

```cpp
Aspose::Words::Saving::OoxmlCompliance Aspose::Words::Document::get_Compliance()
```

## Remarks


If you created a new blank document or load non OOXML document returns the [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/) value.

## Examples



Shows how to read a loaded document's Open Office XML compliance version. 
```cpp
// The compliance version varies between documents created by different versions of Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.doc");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Ecma376_2006);

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);
```

## See Also

* Enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
