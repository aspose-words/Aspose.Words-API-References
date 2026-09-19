---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML metodo"
linktitle: "get_WordOpenXML"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML. Restituisce una stringa che rappresenta l'XML contenuto nel nodo nel formato FlatOpc in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words.markup/istructureddocumenttag/get_wordopenxml/
---
## IStructuredDocumentTag::get_WordOpenXML method


Restituisce una stringa che rappresenta l'XML contenuto nel nodo nel formato [FlatOpc](../../../aspose.words/saveformat/).

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML()=0
```


## Esempi



Mostra come ottenere l'XML contenuto nel nodo nel formato FlatOpc.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_TRUE(tags->idx_get(0)->get_WordOpenXML().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

## Vedi anche

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
