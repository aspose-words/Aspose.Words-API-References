---
title: "Aspose::Words::Fonts::FontInfo::GetEmbeddedFont Methode"
linktitle: "GetEmbeddedFont"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontInfo::GetEmbeddedFont Methode. Ruft eine bestimmte eingebettete Schriftdatei in C++ ab."
type: docs
weight: 9000
url: /de/cpp/aspose.words.fonts/fontinfo/getembeddedfont/
---
## FontInfo::GetEmbeddedFont method


Ruft eine bestimmte eingebettete Schriftdatei ab.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Fonts::FontInfo::GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat format, Aspose::Words::Fonts::EmbeddedFontStyle style)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Format | Aspose::Words::Fonts::EmbeddedFontFormat | Gibt das abzurufende Schriftformat an. |
| Stil | Aspose::Words::Fonts::EmbeddedFontStyle | Gibt den abzurufenden Schriftstil an. |

### ReturnValue

Gibt **null** zurück, wenn die angegebene Schriftart nicht eingebettet ist.

## Beispiele



Zeigt, wie man eine eingebettete Schriftart aus einem Dokument extrahiert und im lokalen Dateisystem speichert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfo> embeddedFont = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift");
System::ArrayPtr<uint8_t> embeddedFontBytes = embeddedFont->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Eingebettete Schriftartformate können in anderen Formaten wie .doc unterschiedlich sein.
// Wir müssen das korrekte Format kennen, bevor wir die Schriftart extrahieren können.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.doc");

ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::EmbeddedOpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));

// Außerdem können wir das eingebettete OpenType-Format, das aus .doc-Dokumenten stammt, in OpenType konvertieren.
embeddedFontBytes = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFontAsOpenType(Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

## Siehe auch

* Enum [EmbeddedFontFormat](../../embeddedfontformat/)
* Enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
