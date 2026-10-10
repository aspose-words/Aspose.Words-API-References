---
title: "Método Aspose::Words::Markup::XmlMapping::get_IsMapped"
linktitle: "get_IsMapped"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Markup::XmlMapping::get_IsMapped. Devuelve true si la etiqueta de documento estructurado principal está asignada correctamente a datos XML en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.markup/xmlmapping/get_ismapped/
---
## XmlMapping::get_IsMapped method


Devuelve **true** si la etiqueta de documento estructurado principal se asigna correctamente a los datos XML.

```cpp
bool Aspose::Words::Markup::XmlMapping::get_IsMapped()
```


## Ejemplos



Muestra cómo establecer asignaciones XML para partes XML personalizadas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Construya una parte XML que contenga texto y agréguela a la colección CustomXmlPart del documento.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// Cree una etiqueta de documento estructurado que mostrará el contenido de nuestro CustomXmlPart.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);

// Establezca una asignación para nuestra etiqueta de documento estructurado. Esta asignación instruirá
// a nuestra etiqueta de documento estructurado que muestre una porción del contenido de texto de la parte XML al que apunta el XPath.
// En este caso, será el contenido del segundo elemento "<text>" del primer elemento "<root>": "Text element #2".
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", u"xmlns:ns='http://www.w3.org/2001/XMLSchema'");

ASSERT_TRUE(tag->get_XmlMapping()->get_IsMapped());
ASPOSE_ASSERT_EQ(xmlPart, tag->get_XmlMapping()->get_CustomXmlPart());
ASSERT_EQ(u"/root[1]/text[2]", tag->get_XmlMapping()->get_XPath());
ASSERT_EQ(u"xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag->get_XmlMapping()->get_PrefixMappings());

// Agregue la etiqueta de documento estructurado al documento para mostrar el contenido de nuestra parte personalizada.
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);
doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.XmlMapping.docx");
```

## Ver también

* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
