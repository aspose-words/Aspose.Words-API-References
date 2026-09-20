---
title: "Перечисление Aspose::Words::Fonts::FontSourceType"
linktitle: "FontSourceType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontSourceType enum. Указывает тип источника шрифтов в C++."
type: docs
weight: 23000
url: /ru/cpp/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enum


Указывает тип источника шрифтов.

```cpp
enum class FontSourceType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| FontFile | 0 | Объект [FileFontSource](../filefontsource/) представляет отдельный файл шрифта. |
| FontsFolder | 1 | Объект [FolderFontSource](../folderfontsource/) представляет папку с файлами шрифтов. |
| MemoryFont | 2 | Объект [MemoryFontSource](../memoryfontsource/) представляет отдельный шрифт в памяти. |
| SystemFonts | 3 | Объект [SystemFontSource](../systemfontsource/) представляет все шрифты, установленные в системе. |
| FontStream | 4 | Объект [StreamFontSource](../streamfontsource/) представляет поток с данными шрифта. |


## Примеры



Показывает, как использовать файл шрифта в локальной файловой системе в качестве источника шрифта.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## См. также

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
