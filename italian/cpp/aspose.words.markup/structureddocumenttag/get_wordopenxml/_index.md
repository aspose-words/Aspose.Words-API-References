---
title: "Metodo Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML"
linktitle: "get_WordOpenXML"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML. Restituisce una stringa che rappresenta l'XML contenuto nel nodo nel formato FlatOpc in C++."
type: docs
weight: 33000
url: /it/cpp/aspose.words.markup/structureddocumenttag/get_wordopenxml/
---
## StructuredDocumentTag::get_WordOpenXML method


Restituisce una stringa che rappresenta l'XML contenuto nel nodo nel formato [FlatOpc](../../../aspose.words/saveformat/).

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML() override
```


## Esempi



Mostra come ottenere l'XML contenuto nel nodo nel formato FlatOpc.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_TRUE(tags->idx_get(0)->get_WordOpenXML().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

## Vedi anche

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
