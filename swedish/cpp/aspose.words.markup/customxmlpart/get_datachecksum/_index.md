---
title: "Aspose::Words::Markup::CustomXmlPart::get_DataChecksum‑metod"
linktitle: "get_DataChecksum"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::CustomXmlPart::get_DataChecksum‑metod. Anger en cyklisk redundanskontroll (CRC) kontrollsumma av Data‑innehållet i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.markup/customxmlpart/get_datachecksum/
---
## CustomXmlPart::get_DataChecksum method


Anger en cyklisk redundanskontroll (CRC) kontrollsumma av [Data](../get_data/)‑innehållet.

```cpp
int64_t Aspose::Words::Markup::CustomXmlPart::get_DataChecksum()
```


## Exempel



Visar hur kontrollsumman beräknas vid körning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto richText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(richText);

// Kontrollsumman är skrivskyddad och beräknas med data från motsvarande anpassade XML‑datapart.
richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>ContentControl</text></root>"), u"/root/text", u"");

int64_t checksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << checksum << std::endl;

richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>Updated ContentControl</text></root>"), u"/root/text", u"");

int64_t updatedChecksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << updatedChecksum << std::endl;

// Vi ändrade XmlPart‑taggen, och kontrollsumman uppdaterades vid körning.
ASSERT_NE(checksum, updatedChecksum);
```

## Se även

* Class [CustomXmlPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
