---
title: "Aspose::Words::Fonts::FileFontSource class"
linktitle: "FileFontSource"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FileFontSource class. Представляет отдельный файл TrueType, хранящийся в файловой системе. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fonts/filefontsource/
---
## FileFontSource class


Представляет отдельный файл TrueType, хранящийся в файловой системе. Чтобы узнать больше, посетите статью документации [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FileFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Методы

| Метод | Описание |
| --- | --- |
| [FileFontSource](./filefontsource/)(const System::String\&) | Конструктор. |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t) | Конструктор. |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t, const System::String\&) | Конструктор. |
| [get_CacheKey](./get_cachekey/)() const | Ключ этого источника в кэше. |
| [get_FilePath](./get_filepath/)() const | Путь к файлу шрифта. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Возвращает приоритет источника шрифтов. |
| [get_Type](./get_type/)() override | Возвращает тип источника шрифтов. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Вызывается во время обработки источника шрифтов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Возвращает список шрифтов, доступных через этот источник. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Вызывается во время обработки источника шрифтов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
| static [Type](./type/)() |  |

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

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
