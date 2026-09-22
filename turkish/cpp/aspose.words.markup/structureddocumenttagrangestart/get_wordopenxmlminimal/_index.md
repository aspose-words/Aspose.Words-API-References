---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal yöntemi"
linktitle: "get_WordOpenXMLMinimal"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal yöntemi. Düğüm içinde FlatOpc formatında bulunan XML'i temsil eden bir dize alır. WordOpenXML özelliğinin aksine, bu yöntem C++'de içerik dışı bölümleri hariç tutan sadeleştirilmiş bir belge oluşturur."
type: docs
weight: 20500
url: /tr/cpp/aspose.words.markup/structureddocumenttagrangestart/get_wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal method


Düğüm içinde bulunan XML'i [FlatOpc](../../../aspose.words/saveformat/) biçiminde temsil eden bir dize alır. [WordOpenXML](../get_wordopenxml/) özelliğinin aksine, bu yöntem içerik dışı bölümleri hariç tutan sadeleştirilmiş bir belge oluşturur.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal()
```


## Örnekler



Düğüm içinde FlatOpc formatında bulunan minimal XML'in nasıl alınacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

ASSERT_TRUE(tag->get_WordOpenXMLMinimal().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
ASSERT_FALSE(tag->get_WordOpenXMLMinimal().Contains(u"xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

## Ayrıca Bakınız

* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
