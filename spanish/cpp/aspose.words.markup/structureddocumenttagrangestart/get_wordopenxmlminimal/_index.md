---
title: "Método Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal"
linktitle: "get_WordOpenXMLMinimal"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal. Obtiene una cadena que representa el XML contenido dentro del nodo en formato FlatOpc. A diferencia de la propiedad WordOpenXML, este método genera un documento simplificado que excluye cualquier parte no relacionada con el contenido en C++."
type: docs
weight: 20500
url: /es/cpp/aspose.words.markup/structureddocumenttagrangestart/get_wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal method


Obtiene una cadena que representa el XML contenido dentro del nodo en el formato [FlatOpc](../../../aspose.words/saveformat/). A diferencia de la propiedad [WordOpenXML](../get_wordopenxml/), este método genera un documento simplificado que excluye cualquier parte no relacionada con el contenido.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal()
```


## Ejemplos



Muestra cómo obtener el XML mínimo contenido dentro del nodo en formato FlatOpc.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

ASSERT_TRUE(tag->get_WordOpenXMLMinimal().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
ASSERT_FALSE(tag->get_WordOpenXMLMinimal().Contains(u"xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

## Ver también

* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
