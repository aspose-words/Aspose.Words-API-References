---
title: "Aspose::Words::Fonts::FontInfo::GetEmbeddedFontAsOpenType metod"
linktitle: "GetEmbeddedFontAsOpenType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontInfo::GetEmbeddedFontAsOpenType metod. Hämtar en inbäddad teckensnittsfil i OpenType-format. Teckensnitt i Embedded OpenType-format konverteras till OpenType i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.fonts/fontinfo/getembeddedfontasopentype/
---
## FontInfo::GetEmbeddedFontAsOpenType method


Hämtar en inbäddad teckensnittsfil i OpenType-format. [Fonts](../../) i Embedded OpenType-format konverteras till OpenType.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Fonts::FontInfo::GetEmbeddedFontAsOpenType(Aspose::Words::Fonts::EmbeddedFontStyle style)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stil | Aspose::Words::Fonts::EmbeddedFontStyle | Anger teckensnittsstilen att hämta. |

### ReturnValue

Returnerar **null** om det angivna teckensnittet inte är inbäddat.

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

* Enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
