---
title: "Aspose::Words::Fonts::EmbeddedFontStyle enum"
linktitle: "EmbeddedFontStyle"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::EmbeddedFontStyle enum. Gibt den Stil einer eingebetteten Schriftart innerhalb eines FontInfo‑Objekts in C++ an."
type: docs
weight: 20000
url: /de/cpp/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enum


Gibt den Stil einer eingebetteten Schriftart innerhalb eines [FontInfo](../fontinfo/) Objekts an.

```cpp
enum class EmbeddedFontStyle
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Regular | 0 | Gibt die reguläre eingebettete Schriftart an. |
| Bold | 1 | Gibt die fette eingebettete Schriftart an. |
| Kursiv | 2 | Gibt die eingebettete Kursiv-Schriftart an. |
| FettKursiv | 3 | Gibt die eingebettete Fett‑Kursiv-Schriftart an. |


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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
