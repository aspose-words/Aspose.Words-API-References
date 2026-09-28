---
title: "Aspose::Words::Fonts::FileFontSource::get_FilePath метод"
linktitle: "get_FilePath"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FileFontSource::get_FilePath метод. Путь к файлу шрифта в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.fonts/filefontsource/get_filepath/
---
## FileFontSource::get_FilePath method


Путь к файлу шрифта.

```cpp
System::String Aspose::Words::Fonts::FileFontSource::get_FilePath() const
```


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

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
