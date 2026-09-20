---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping method"
linktitle: "get_XmlMapping"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping method. Obtiene un objeto que representa el mapeo de este rango de etiqueta de documento estructurado a datos XML en una parte XML personalizada del documento actual en C++."
type: docs
weight: 21000
url: /es/cpp/aspose.words.markup/structureddocumenttagrangestart/get_xmlmapping/
---
## StructuredDocumentTagRangeStart::get_XmlMapping method


Obtiene un objeto que representa el mapeo de este rango de etiqueta de documento estructurado a datos XML en una parte XML personalizada del documento actual.

```cpp
System::SharedPtr<Aspose::Words::Markup::XmlMapping> Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping() override
```


## Ejemplos



Muestra cómo establecer mapeos XML para el inicio de rango de una etiqueta de documento estructurado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

// Construya una parte XML que contenga texto y agréguela a la colección CustomXmlPart del documento.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// Cree una etiqueta de documento estructurado que mostrará el contenido de nuestro CustomXmlPart en el documento.
auto sdtRangeStart = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

// Si establecemos un mapeo para nuestra etiqueta de documento estructurado,
// solo mostrará una parte del CustomXmlPart a la que apunta el XPath.
// Este XPath apuntará al segundo elemento "<text>" del contenido del primer elemento "<root>" de nuestro CustomXmlPart.
sdtRangeStart->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", nullptr);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

## Ver también

* Class [XmlMapping](../../xmlmapping/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
