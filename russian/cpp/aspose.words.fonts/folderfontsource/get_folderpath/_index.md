---
title: "метод Aspose::Words::Fonts::FolderFontSource::get_FolderPath"
linktitle: "get_FolderPath"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Fonts::FolderFontSource::get_FolderPath. Путь к папке в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.fonts/folderfontsource/get_folderpath/
---
## FolderFontSource::get_FolderPath method


Путь к папке.

```cpp
System::String Aspose::Words::Fonts::FolderFontSource::get_FolderPath() const
```


## Примеры



Показывает, как использовать локальную системную папку, содержащую шрифты, в качестве источника шрифтов.
```cpp
// Создайте источник шрифтов из папки, содержащей файлы шрифтов.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## См. также

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
