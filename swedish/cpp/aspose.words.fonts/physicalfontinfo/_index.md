---
title: "Aspose::Words::Fonts::PhysicalFontInfo klass"
linktitle: "PhysicalFontInfo"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::PhysicalFontInfo klass. Anger information om fysiskt teckensnitt som är tillgängligt för Aspose.Words teckensnittsmotor. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 15000
url: /sv/cpp/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class


Specificerar information om fysiskt teckensnitt som är tillgängligt för Aspose.Words teckensnittsmotor. För att lära dig mer, besök dokumentationsartikeln [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class PhysicalFontInfo : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() const | Inbäddning av licensrättigheter för teckensnittet. |
| [get_FilePath](./get_filepath/)() const | Sökväg till teckensnittsfilen, om någon. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | Familjenamn för teckensnittet. |
| [get_FullFontName](./get_fullfontname/)() const | Fullständigt namn för teckensnittet. |
| [get_Version](./get_version/)() const | Versionssträng för teckensnittet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Exempel



Visar hur man listar tillgängliga teckensnitt.
```cpp
// Konfigurera Aspose.Words för att hämta teckensnitt från en anpassad mapp, och skriv sedan ut varje tillgängligt teckensnitt.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> folderFontSource = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true)});

for (auto&& fontInfo : System::IterateOver(folderFontSource[0]->GetAvailableFonts()))
{
    std::cout << "FontFamilyName : " << fontInfo->get_FontFamilyName() << std::endl;
    std::cout << "FullFontName  : " << fontInfo->get_FullFontName() << std::endl;
    std::cout << "Version  : " << fontInfo->get_Version() << std::endl;
    std::cout << "FilePath : " << fontInfo->get_FilePath() << "\n" << std::endl;
}
```

## Se även

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
