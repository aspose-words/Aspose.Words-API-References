---
title: "Aspose::Words::Fonts::EmbeddedFontFormat enum"
linktitle: "EmbeddedFontFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::EmbeddedFontFormat enum. Anger formatet för ett specifikt inbäddat teckensnitt i FontInfo-objektet. När ett dokument sparas till en fil skrivs endast inbäddade teckensnitt av motsvarande format ner i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enum


Anger formatet för ett specifikt inbäddat teckensnitt i [FontInfo](../fontinfo/)-objektet. När ett dokument sparas till en fil skrivs endast inbäddade teckensnitt av motsvarande format ner.

```cpp
enum class EmbeddedFontFormat
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| EmbeddedOpenType | 0 | Anger Embedded OpenType (EOT) filformat. Detta format för inbäddade teckensnitt används i DOC-filer. |
| OpenType | 1 | Anger teckensnitt, inbäddat som en enkel kopia av OpenType (TrueType)-teckensnittfilen. Detta format för inbäddade teckensnitt används i Open Office XML-format, inklusive DOCX-filer. |


## Exempel



Visar hur man extraherar ett inbäddat teckensnitt från ett dokument och sparar det till den lokala filsystemet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfo> embeddedFont = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift");
System::ArrayPtr<uint8_t> embeddedFontBytes = embeddedFont->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Inbäddade teckensnittformat kan vara olika i andra format såsom .doc.
// Vi måste veta rätt format innan vi kan extrahera teckensnittet.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.doc");

ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::EmbeddedOpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));

// Vi kan också konvertera inbäddat OpenType‑format, som kommer från .doc‑dokument, till OpenType.
embeddedFontBytes = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFontAsOpenType(Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

## Se även

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
