---
title: "Método get_DataChecksum de Aspose::Words::Markup::CustomXmlPart"
linktitle: "get_DataChecksum"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método get_DataChecksum de Aspose::Words::Markup::CustomXmlPart. Especifica una suma de verificación de redundancia cíclica (CRC) del contenido Data en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.markup/customxmlpart/get_datachecksum/
---
## CustomXmlPart::get_DataChecksum method


Especifica una suma de verificación de redundancia cíclica (CRC) del contenido [Data](../get_data/).

```cpp
int64_t Aspose::Words::Markup::CustomXmlPart::get_DataChecksum()
```


## Ejemplos



Muestra cómo se calcula la suma de verificación en tiempo de ejecución.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto richText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(richText);

// La suma de verificación es de solo lectura y se calcula usando los datos de la parte XML personalizada correspondiente.
richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>ContentControl</text></root>"), u"/root/text", u"");

int64_t checksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << checksum << std::endl;

richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>Updated ContentControl</text></root>"), u"/root/text", u"");

int64_t updatedChecksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << updatedChecksum << std::endl;

// Cambió la XmlPart de la etiqueta, y la suma de verificación se actualizó en tiempo de ejecución.
ASSERT_NE(checksum, updatedChecksum);
```

## Ver también

* Class [CustomXmlPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
