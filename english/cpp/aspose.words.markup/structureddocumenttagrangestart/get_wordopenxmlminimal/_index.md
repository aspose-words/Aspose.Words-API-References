---
title: Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal method
linktitle: get_WordOpenXMLMinimal
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal method. Gets a string that represents the XML contained within the node in the FlatOpc format. Unlike the WordOpenXML property, this method generates a stripped-down document that excludes any non-content-related parts in C++.'
type: docs
weight: 20500
url: /cpp/aspose.words.markup/structureddocumenttagrangestart/get_wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal method


Gets a string that represents the XML contained within the node in the [FlatOpc](../../../aspose.words/saveformat/) format. Unlike the [WordOpenXML](../get_wordopenxml/) property, this method generates a stripped-down document that excludes any non-content-related parts.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal()
```


## Examples



Shows how to get minimal XML contained within the node in the FlatOpc format. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

ASSERT_TRUE(tag->get_WordOpenXMLMinimal().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
ASSERT_FALSE(tag->get_WordOpenXMLMinimal().Contains(u"xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

## See Also

* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
