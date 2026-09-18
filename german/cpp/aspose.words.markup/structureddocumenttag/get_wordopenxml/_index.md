---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML Methode"
linktitle: "get_WordOpenXML"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML Methode. Gibt eine Zeichenkette zurück, die das XML darstellt, das im Knoten im FlatOpc-Format in C++ enthalten ist."
type: docs
weight: 33000
url: /de/cpp/aspose.words.markup/structureddocumenttag/get_wordopenxml/
---
## StructuredDocumentTag::get_WordOpenXML method


Gibt eine Zeichenkette zurück, die das im Knoten enthaltene XML im [FlatOpc](../../../aspose.words/saveformat/)-Format darstellt.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML() override
```


## Beispiele



Zeigt, wie man das im Knoten enthaltene XML im FlatOpc-Format abruft.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_TRUE(tags->idx_get(0)->get_WordOpenXML().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

## Siehe auch

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
