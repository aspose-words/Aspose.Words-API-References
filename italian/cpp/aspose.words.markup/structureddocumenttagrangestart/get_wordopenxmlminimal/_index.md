---
title: "Metodo Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal"
linktitle: "get_WordOpenXMLMinimal"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal. Restituisce una stringa che rappresenta l'XML contenuto nel nodo nel formato FlatOpc. A differenza della proprietà WordOpenXML, questo metodo genera un documento semplificato che esclude tutte le parti non relative al contenuto in C++."
type: docs
weight: 20500
url: /it/cpp/aspose.words.markup/structureddocumenttagrangestart/get_wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal method


Restituisce una stringa che rappresenta l'XML contenuto nel nodo nel formato [FlatOpc](../../../aspose.words/saveformat/). A differenza della proprietà [WordOpenXML](../get_wordopenxml/), questo metodo genera un documento semplificato che esclude tutte le parti non relative al contenuto.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal()
```


## Esempi



Mostra come ottenere l'XML minimale contenuto nel nodo nel formato FlatOpc.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

ASSERT_TRUE(tag->get_WordOpenXMLMinimal().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
ASSERT_FALSE(tag->get_WordOpenXMLMinimal().Contains(u"xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

## Vedi anche

* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
