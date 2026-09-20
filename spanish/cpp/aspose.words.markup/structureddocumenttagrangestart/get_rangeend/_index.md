---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_RangeEnd método"
linktitle: "get_RangeEnd"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_RangeEnd método. Especifica el final del rango si el StructuredDocumentTag es una etiqueta de documento estructurada con rango. De lo contrario, devuelve null en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words.markup/structureddocumenttagrangestart/get_rangeend/
---
## StructuredDocumentTagRangeStart::get_RangeEnd method


Especifica el final del rango si el [StructuredDocumentTag](../../structureddocumenttag/) es una etiqueta de documento estructurada con rango. De lo contrario, devuelve **null**.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTagRangeEnd> Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_RangeEnd()
```


## Ejemplos



Muestra cómo obtener las propiedades de etiquetas de documento estructurado de varias secciones.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

auto rangeStartTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));
auto rangeEndTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeEnd>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeEnd, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeStartTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|Title: {0}", rangeStartTag->get_Title()) << std::endl;
std::cout << System::String::Format(u"\t|PlaceholderName: {0}", rangeStartTag->get_PlaceholderName()) << std::endl;
std::cout << System::String::Format(u"\t|IsShowingPlaceholderText: {0}", rangeStartTag->get_IsShowingPlaceholderText()) << std::endl;
std::cout << System::String::Format(u"\t|LockContentControl: {0}", rangeStartTag->get_LockContentControl()) << std::endl;
std::cout << System::String::Format(u"\t|LockContents: {0}", rangeStartTag->get_LockContents()) << std::endl;
std::cout << System::String::Format(u"\t|Level: {0}", rangeStartTag->get_Level()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeStartTag->get_NodeType()) << std::endl;
std::cout << System::String::Format(u"\t|RangeEnd: {0}", rangeStartTag->get_RangeEnd()) << std::endl;
std::cout << System::String::Format(u"\t|Color: {0}", rangeStartTag->get_Color().ToArgb()) << std::endl;
std::cout << System::String::Format(u"\t|SdtType: {0}", rangeStartTag->get_SdtType()) << std::endl;
std::cout << System::String::Format(u"\t|FlatOpcContent: {0}", rangeStartTag->get_WordOpenXML()) << std::endl;
std::cout << System::String::Format(u"\t|Tag: {0}\n", rangeStartTag->get_Tag()) << std::endl;

std::cout << "StructuredDocumentTagRangeEnd values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeEndTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeEndTag->get_NodeType()) << std::endl;
```

## Ver también

* Class [StructuredDocumentTagRangeEnd](../../structureddocumenttagrangeend/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
