---
title: "Aspose::Words::Fonts::FolderFontSource klass"
linktitle: "FolderFontSource"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FolderFontSource klass. Representerar mappen som innehåller TrueType‑teckensnittsfiler. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class


Representerar mappen som innehåller TrueType‑teckensnittsfiler. För att lära dig mer, besök dokumentationsartikeln [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FolderFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool) | Konstruktör. |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool, int32_t) | Konstruktör. |
| [get_FolderPath](./get_folderpath/)() const | Sökväg till mappen. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Returnerar prioriteten för teckensnittskällan. |
| [get_ScanSubfolders](./get_scansubfolders/)() const | Bestämmer om underkataloger ska genomsökas eller inte. |
| [get_Type](./get_type/)() override | Returnerar typen av teckensnittskälla. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Kallas under bearbetning av teckensnittskällan när ett problem upptäcks som kan leda till förlust av formateringsnoggrannhet. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Returnerar en lista över teckensnitt som är tillgängliga via denna källa. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Kallas under bearbetning av teckensnittskällan när ett problem upptäcks som kan leda till förlust av formateringsnoggrannhet. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man använder en lokal systemmapp som innehåller teckensnitt som en teckensnittskälla.
```cpp
// Skapa en teckensnittskälla från en mapp som innehåller teckensnittsfiler.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## Se även

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
