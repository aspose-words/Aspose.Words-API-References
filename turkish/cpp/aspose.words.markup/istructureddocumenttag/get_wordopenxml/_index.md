---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML method"
linktitle: "get_WordOpenXML"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML metodu. C++'ta FlatOpc formatında düğüm içinde bulunan XML'i temsil eden bir dize alır."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.markup/istructureddocumenttag/get_wordopenxml/
---
## IStructuredDocumentTag::get_WordOpenXML method


Düğüm içinde bulunan XML'i temsil eden bir dize alır [FlatOpc](../../../aspose.words/saveformat/) formatında.

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML()=0
```


## Örnekler



FlatOpc formatında düğüm içinde bulunan XML'i nasıl alacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_TRUE(tags->idx_get(0)->get_WordOpenXML().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

## Ayrıca Bakınız

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
