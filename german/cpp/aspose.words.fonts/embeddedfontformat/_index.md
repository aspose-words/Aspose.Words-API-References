---
title: "Aspose::Words::Fonts::EmbeddedFontFormat Enum"
linktitle: "EmbeddedFontFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::EmbeddedFontFormat Enum. Gibt das Format einer bestimmten eingebetteten Schriftart im FontInfo-Objekt an. Beim Speichern eines Dokuments in einer Datei werden nur eingebettete Schriftarten des entsprechenden Formats in C++ geschrieben."
type: docs
weight: 19000
url: /de/cpp/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enum


Gibt das Format einer bestimmten eingebetteten Schriftart im [FontInfo](../fontinfo/)-Objekt an. Beim Speichern eines Dokuments in einer Datei werden nur eingebettete Schriftarten des entsprechenden Formats geschrieben.

```cpp
enum class EmbeddedFontFormat
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| EmbeddedOpenType | 0 | Gibt das Embedded OpenType (EOT)-Dateiformat an. Dieses Format eingebetteter Schriften wird in DOC-Dateien verwendet. |
| OpenType | 1 | Gibt die Schriftart an, eingebettet als einfache Kopie einer OpenType (TrueType)-Schriftdatei. Dieses Format eingebetteter Schriften wird im Open Office XML-Format, einschließlich DOCX-Dateien, verwendet. |


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
