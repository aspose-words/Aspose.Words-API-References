---
title: "Aspose::Words::Fonts::FontInfo Klasse"
linktitle: "FontInfo"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontInfo Klasse. Gibt Informationen über eine im Dokument verwendete Schrift an. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.fonts/fontinfo/
---
## FontInfo class


Gibt Informationen über eine im Dokument verwendete Schriftart an. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontInfo : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_AltName](./get_altname/)() const | Liest oder setzt den alternativen Namen der Schrift. |
| [get_Charset](./get_charset/)() | Liest oder setzt den Zeichensatz der Schrift. |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() | Liest die Lizenzrechte der eingebetteten Schrift. |
| [get_Family](./get_family/)() const | Liest oder setzt die Schriftfamilie, zu der diese Schrift gehört. |
| [get_IsTrueType](./get_istruetype/)() const | Gibt an, dass diese Schrift eine TrueType- oder OpenType-Schrift ist, im Gegensatz zu einer Raster- oder Vektorschrift. Standardwert ist **true**. |
| [get_Name](./get_name/)() const | Liest den Namen der Schrift. |
| [get_Panose](./get_panose/)() const | Liest oder setzt die PANOSE-Schriftklassifizierungsnummer. |
| [get_Pitch](./get_pitch/)() const | Die Schriftbreite gibt an, ob die Schrift festbreit, proportional verteilt oder von einer Standardeinstellung abhängig ist. |
| [GetEmbeddedFont](./getembeddedfont/)(Aspose::Words::Fonts::EmbeddedFontFormat, Aspose::Words::Fonts::EmbeddedFontStyle) | Ruft eine bestimmte eingebettete Schriftdatei ab. |
| [GetEmbeddedFontAsOpenType](./getembeddedfontasopentype/)(Aspose::Words::Fonts::EmbeddedFontStyle) | Ruft eine eingebettete Schriftdatei im OpenType-Format ab. [Fonts](../) im Embedded OpenType-Format werden in OpenType konvertiert. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AltName](./set_altname/)(const System::String\&) | Setter für [Aspose::Words::Fonts::FontInfo::get_AltName](./get_altname/). |
| [set_Charset](./set_charset/)(int32_t) | Setter für [Aspose::Words::Fonts::FontInfo::get_Charset](./get_charset/). |
| [set_Family](./set_family/)(Aspose::Words::Fonts::FontFamily) | Setter für [Aspose::Words::Fonts::FontInfo::get_Family](./get_family/). |
| [set_IsTrueType](./set_istruetype/)(bool) | Setter für [Aspose::Words::Fonts::FontInfo::get_IsTrueType](./get_istruetype/). |
| [set_Panose](./set_panose/)(const System::ArrayPtr\<uint8_t\>\&) | Setter für [Aspose::Words::Fonts::FontInfo::get_Panose](./get_panose/). |
| [set_Pitch](./set_pitch/)(Aspose::Words::Fonts::FontPitch) | Setter für [Aspose::Words::Fonts::FontInfo::get_Pitch](./get_pitch/). |
| static [Type](./type/)() |  |
## Hinweise


Sie erstellen keine Instanzen dieser Klasse direkt. Verwenden Sie die Eigenschaft [FontInfos](../../aspose.words/documentbase/get_fontinfos/), um auf die Sammlung von im Dokument definierten Schriften zuzugreifen.

## Beispiele



Zeigt, wie man die Details der im Dokument vorhandenen Schriften ausgibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Gibt alle verwendeten und nicht verwendeten Schriften im Dokument aus.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```

## Siehe auch

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
