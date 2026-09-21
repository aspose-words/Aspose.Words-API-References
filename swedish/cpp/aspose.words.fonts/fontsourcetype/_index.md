---
title: "Aspose::Words::Fonts::FontSourceType enum"
linktitle: "FontSourceType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontSourceType enum. Anger typen av teckensnittskälla i C++."
type: docs
weight: 23000
url: /sv/cpp/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enum


Specificerar typen av teckensnittskälla.

```cpp
enum class FontSourceType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| FontFile | 0 | Ett [FileFontSource](../filefontsource/)‑objekt som representerar en enskild teckensnittfil. |
| FontsFolder | 1 | Ett [FolderFontSource](../folderfontsource/)‑objekt som representerar en mapp med teckensnittsfiler. |
| MemoryFont | 2 | Ett [MemoryFontSource](../memoryfontsource/)‑objekt som representerar ett enskilt teckensnitt i minnet. |
| SystemFonts | 3 | Ett [SystemFontSource](../systemfontsource/)‑objekt som representerar alla teckensnitt som är installerade i systemet. |
| FontStream | 4 | Ett [StreamFontSource](../streamfontsource/)‑objekt som representerar en ström med teckensnittsdata. |


## Exempel



Visar hur man använder en typsnittfil i det lokala filsystemet som en typsnittskälla.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## Se även

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
