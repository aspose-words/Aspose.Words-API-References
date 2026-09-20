---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML método"
linktitle: "get_WordOpenXML"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML método. Obtiene una cadena que representa el XML contenido dentro del nodo en el formato FlatOpc en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.markup/istructureddocumenttag/get_wordopenxml/
---
## IStructuredDocumentTag::get_WordOpenXML method


Obtiene una cadena que representa el XML contenido dentro del nodo en el formato [FlatOpc](../../../aspose.words/saveformat/).

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML()=0
```


## Ejemplos



Muestra cómo obtener el XML contenido dentro del nodo en el formato FlatOpc.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_TRUE(tags->idx_get(0)->get_WordOpenXML().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

## Ver también

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
