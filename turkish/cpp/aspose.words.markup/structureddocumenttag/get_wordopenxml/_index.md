---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML metodu"
linktitle: "get_WordOpenXML"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML metodu. C++'ta FlatOpc formatında düğüm içinde bulunan XML'i temsil eden bir dize alır."
type: docs
weight: 33000
url: /tr/cpp/aspose.words.markup/structureddocumenttag/get_wordopenxml/
---
## StructuredDocumentTag::get_WordOpenXML method


Düğüm içinde bulunan XML'i temsil eden bir dize alır [FlatOpc](../../../aspose.words/saveformat/) formatında.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML() override
```


## Örnekler



FlatOpc formatında düğüm içinde bulunan XML'i nasıl alacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_TRUE(tags->idx_get(0)->get_WordOpenXML().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

## Ayrıca Bakınız

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
