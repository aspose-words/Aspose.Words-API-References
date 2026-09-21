---
title: "Aspose::Words::Fonts::FontInfo klass"
linktitle: "FontInfo"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontInfo-klass. Anger information om ett teckensnitt som används i dokumentet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.fonts/fontinfo/
---
## FontInfo class


Anger information om ett teckensnitt som används i dokumentet. För att lära dig mer, besök dokumentationsartikeln [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontInfo : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_AltName](./get_altname/)() const | Hämtar eller anger det alternativa namnet för teckensnittet. |
| [get_Charset](./get_charset/)() | Hämtar eller anger teckenuppsättningen för teckensnittet. |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() | Hämtar de inbäddade teckensnittens licensrättigheter. |
| [get_Family](./get_family/)() const | Hämtar eller anger teckensnittsfamiljen som detta teckensnitt tillhör. |
| [get_IsTrueType](./get_istruetype/)() const | Indikerar att detta teckensnitt är ett TrueType- eller OpenType-teckensnitt till skillnad från ett raster- eller vektorteckensnitt. Standard är **true**. |
| [get_Name](./get_name/)() const | Hämtar teckensnittets namn. |
| [get_Panose](./get_panose/)() const | Hämtar eller anger PANOSE-typsnittsklassificeringsnumret. |
| [get_Pitch](./get_pitch/)() const | Pitch indikerar om teckensnittet har fast bredd, proportionellt avstånd eller förlitar sig på en standardinställning. |
| [GetEmbeddedFont](./getembeddedfont/)(Aspose::Words::Fonts::EmbeddedFontFormat, Aspose::Words::Fonts::EmbeddedFontStyle) | Hämtar en specifik inbäddad teckensnittfil. |
| [GetEmbeddedFontAsOpenType](./getembeddedfontasopentype/)(Aspose::Words::Fonts::EmbeddedFontStyle) | Hämtar en inbäddad teckensnittfil i OpenType-format. [Fonts](../) i Embedded OpenType-format konverteras till OpenType. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AltName](./set_altname/)(const System::String\&) | Sättare för [Aspose::Words::Fonts::FontInfo::get_AltName](./get_altname/). |
| [set_Charset](./set_charset/)(int32_t) | Sättare för [Aspose::Words::Fonts::FontInfo::get_Charset](./get_charset/). |
| [set_Family](./set_family/)(Aspose::Words::Fonts::FontFamily) | Sättare för [Aspose::Words::Fonts::FontInfo::get_Family](./get_family/). |
| [set_IsTrueType](./set_istruetype/)(bool) | Sättare för [Aspose::Words::Fonts::FontInfo::get_IsTrueType](./get_istruetype/). |
| [set_Panose](./set_panose/)(const System::ArrayPtr\<uint8_t\>\&) | Sättare för [Aspose::Words::Fonts::FontInfo::get_Panose](./get_panose/). |
| [set_Pitch](./set_pitch/)(Aspose::Words::Fonts::FontPitch) | Sättare för [Aspose::Words::Fonts::FontInfo::get_Pitch](./get_pitch/). |
| static [Type](./type/)() |  |
## Anmärkningar


Du skapar inte instanser av den här klassen direkt. Använd egenskapen [FontInfos](../../aspose.words/documentbase/get_fontinfos/) för att komma åt samlingen av teckensnitt som definieras i ett dokument.

## Exempel



Visar hur man skriver ut detaljerna för vilka teckensnitt som finns i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Skriv ut alla använda och oanvända teckensnitt i dokumentet.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```

## Se även

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
