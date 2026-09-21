---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal metod"
linktitle: "get_WordOpenXMLMinimal"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal-metoden. Hämtar en sträng som representerar XML som finns i noden i FlatOpc-formatet. Till skillnad från WordOpenXML-egenskapen genererar den här metoden ett nedskalad dokument som utesluter alla icke-innehållsrelaterade delar i C++."
type: docs
weight: 20500
url: /sv/cpp/aspose.words.markup/structureddocumenttagrangestart/get_wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal method


Hämtar en sträng som representerar XML som finns i noden i [FlatOpc](../../../aspose.words/saveformat/)-formatet. Till skillnad från [WordOpenXML](../get_wordopenxml/)-egenskapen genererar den här metoden ett nedskalat dokument som utesluter alla icke‑innehållsrelaterade delar.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal()
```


## Exempel



Visar hur man får minimal XML som finns i noden i FlatOpc-formatet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

ASSERT_TRUE(tag->get_WordOpenXMLMinimal().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
ASSERT_FALSE(tag->get_WordOpenXMLMinimal().Contains(u"xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

## Se även

* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
