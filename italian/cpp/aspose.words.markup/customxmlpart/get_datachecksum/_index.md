---
title: "Aspose::Words::Markup::CustomXmlPart::get_DataChecksum metodo"
linktitle: "get_DataChecksum"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::CustomXmlPart::get_DataChecksum metodo. Specifica un checksum di controllo di ridondanza ciclica (CRC) del contenuto Data in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.markup/customxmlpart/get_datachecksum/
---
## CustomXmlPart::get_DataChecksum method


Specifica un checksum di controllo di ridondanza ciclica (CRC) del contenuto [Data](../get_data/).

```cpp
int64_t Aspose::Words::Markup::CustomXmlPart::get_DataChecksum()
```


## Esempi



Mostra come il checksum viene calcolato a runtime.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto richText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(richText);

// Il checksum è di sola lettura e viene calcolato usando i dati della corrispondente parte XML personalizzata.
richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>ContentControl</text></root>"), u"/root/text", u"");

int64_t checksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << checksum << std::endl;

richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>Updated ContentControl</text></root>"), u"/root/text", u"");

int64_t updatedChecksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << updatedChecksum << std::endl;

// Abbiamo modificato l'XmlPart del tag e il checksum è stato aggiornato a runtime.
ASSERT_NE(checksum, updatedChecksum);
```

## Vedi anche

* Class [CustomXmlPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
