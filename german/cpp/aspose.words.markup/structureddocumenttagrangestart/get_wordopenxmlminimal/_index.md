---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal Methode"
linktitle: "get_WordOpenXMLMinimal"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal Methode. Gibt einen String zurück, der das XML darstellt, das im Knoten im FlatOpc-Format enthalten ist. Im Gegensatz zur WordOpenXML-Eigenschaft erzeugt diese Methode ein vereinfachtes Dokument, das alle nicht inhaltlichen Teile ausschließt, in C++."
type: docs
weight: 20500
url: /de/cpp/aspose.words.markup/structureddocumenttagrangestart/get_wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal method


Gibt eine Zeichenkette zurück, die das XML darstellt, das im Knoten im [FlatOpc](../../../aspose.words/saveformat/)-Format enthalten ist. Im Gegensatz zur [WordOpenXML](../get_wordopenxml/)-Eigenschaft erzeugt diese Methode ein reduziertes Dokument, das alle nicht inhaltbezogenen Teile ausschließt.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal()
```


## Beispiele



Zeigt, wie man das minimale XML, das im Knoten im FlatOpc-Format enthalten ist, erhält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

ASSERT_TRUE(tag->get_WordOpenXMLMinimal().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
ASSERT_FALSE(tag->get_WordOpenXMLMinimal().Contains(u"xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

## Siehe auch

* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
