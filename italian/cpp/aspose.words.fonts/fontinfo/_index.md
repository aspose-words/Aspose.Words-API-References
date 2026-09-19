---
title: "Aspose::Words::Fonts::FontInfo classe"
linktitle: "FontInfo"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontInfo classe. Specifica le informazioni su un font utilizzato nel documento. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.fonts/fontinfo/
---
## FontInfo class


Specifica le informazioni su un carattere utilizzato nel documento. Per saperne di più, visita l'articolo di documentazione [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontInfo : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_AltName](./get_altname/)() const | Ottiene o imposta il nome alternativo per il font. |
| [get_Charset](./get_charset/)() | Ottiene o imposta il set di caratteri per il font. |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() | Ottiene i diritti di licenza del font incorporato. |
| [get_Family](./get_family/)() const | Ottiene o imposta la famiglia di font a cui appartiene questo font. |
| [get_IsTrueType](./get_istruetype/)() const | Indica che questo font è un font TrueType o OpenType, a differenza di un font raster o vettoriale. Il valore predefinito è **true**. |
| [get_Name](./get_name/)() const | Ottiene il nome del carattere. |
| [get_Panose](./get_panose/)() const | Ottiene o imposta il numero di classificazione del tipo di carattere PANOSE. |
| [get_Pitch](./get_pitch/)() const | Il pitch indica se il carattere è a larghezza fissa, a spaziatura proporzionale o si basa su un'impostazione predefinita. |
| [GetEmbeddedFont](./getembeddedfont/)(Aspose::Words::Fonts::EmbeddedFontFormat, Aspose::Words::Fonts::EmbeddedFontStyle) | Ottiene un file di carattere incorporato specifico. |
| [GetEmbeddedFontAsOpenType](./getembeddedfontasopentype/)(Aspose::Words::Fonts::EmbeddedFontStyle) | Ottiene un file di carattere incorporato in formato OpenType. [Fonts](../) in formato Embedded OpenType vengono convertiti in OpenType. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AltName](./set_altname/)(const System::String\&) | Impostatore per [Aspose::Words::Fonts::FontInfo::get_AltName](./get_altname/). |
| [set_Charset](./set_charset/)(int32_t) | Impostatore per [Aspose::Words::Fonts::FontInfo::get_Charset](./get_charset/). |
| [set_Family](./set_family/)(Aspose::Words::Fonts::FontFamily) | Impostatore per [Aspose::Words::Fonts::FontInfo::get_Family](./get_family/). |
| [set_IsTrueType](./set_istruetype/)(bool) | Impostatore per [Aspose::Words::Fonts::FontInfo::get_IsTrueType](./get_istruetype/). |
| [set_Panose](./set_panose/)(const System::ArrayPtr\<uint8_t\>\&) | Impostatore per [Aspose::Words::Fonts::FontInfo::get_Panose](./get_panose/). |
| [set_Pitch](./set_pitch/)(Aspose::Words::Fonts::FontPitch) | Impostatore per [Aspose::Words::Fonts::FontInfo::get_Pitch](./get_pitch/). |
| static [Type](./type/)() |  |
## Note


Non si creano istanze di questa classe direttamente. Utilizzare la proprietà [FontInfos](../../aspose.words/documentbase/get_fontinfos/) per accedere alla raccolta di caratteri definiti in un documento.

## Esempi



Mostra come stampare i dettagli dei caratteri presenti in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Stampa tutti i caratteri utilizzati e non utilizzati nel documento.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```

## Vedi anche

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
