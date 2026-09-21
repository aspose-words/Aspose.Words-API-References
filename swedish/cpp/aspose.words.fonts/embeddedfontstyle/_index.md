---
title: "Aspose::Words::Fonts::EmbeddedFontStyle enum"
linktitle: "EmbeddedFontStyle"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::EmbeddedFontStyle enum. Anger stilen för ett inbäddat teckensnitt i ett FontInfo‑objekt i C++."
type: docs
weight: 20000
url: /sv/cpp/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enum


Anger stilen för ett inbäddat teckensnitt i ett [FontInfo](../fontinfo/)‑objekt.

```cpp
enum class EmbeddedFontStyle
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Regular | 0 | Anger det reguljära inbäddade teckensnittet. |
| Bold | 1 | Anger det fetstilade inbäddade teckensnittet. |
| Italic | 2 | Anger det kursiva inbäddade teckensnittet. |
| BoldItalic | 3 | Anger det fet‑kursiva inbäddade teckensnittet. |


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
