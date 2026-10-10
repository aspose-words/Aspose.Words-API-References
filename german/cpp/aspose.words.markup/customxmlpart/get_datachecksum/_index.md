---
title: "Aspose::Words::Markup::CustomXmlPart::get_DataChecksum Methode"
linktitle: "get_DataChecksum"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::CustomXmlPart::get_DataChecksum Methode. Gibt eine zyklische Redundanzprüfung (CRC) Prüfsumme des Data‑Inhalts in C++ an."
type: docs
weight: 5000
url: /de/cpp/aspose.words.markup/customxmlpart/get_datachecksum/
---
## CustomXmlPart::get_DataChecksum method


Gibt eine zyklische Redundanzprüfung (CRC) Prüfsumme des [Data](../get_data/) Inhalts an.

```cpp
int64_t Aspose::Words::Markup::CustomXmlPart::get_DataChecksum()
```


## Beispiele



Zeigt, wie die Prüfsumme zur Laufzeit berechnet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto richText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(richText);

// Die Prüfsumme ist schreibgeschützt und wird anhand der Daten des entsprechenden benutzerdefinierten XML‑Datenparts berechnet.
richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>ContentControl</text></root>"), u"/root/text", u"");

int64_t checksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << checksum << std::endl;

richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>Updated ContentControl</text></root>"), u"/root/text", u"");

int64_t updatedChecksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << updatedChecksum << std::endl;

// Wir haben das XmlPart des Tags geändert, und die Prüfsumme wurde zur Laufzeit aktualisiert.
ASSERT_NE(checksum, updatedChecksum);
```

## Siehe auch

* Class [CustomXmlPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
