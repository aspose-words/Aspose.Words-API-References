---
title: "Aspose::Words::Fonts::FontSourceBase class"
linktitle: "FontSourceBase"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontSourceBase class. Это абстрактный базовый класс для классов, позволяющих пользователю указывать различные источники шрифтов. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class


Это абстрактный базовый класс для классов, позволяющих пользователю указывать различные источники шрифтов. Чтобы узнать больше, посетите статью документации [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontSourceBase : public Aspose::Fonts::IFontSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Priority](./get_priority/)() const | Возвращает приоритет источника шрифтов. |
| virtual [get_Type](./get_type/)() | Возвращает тип источника шрифтов. |
| [get_WarningCallback](./get_warningcallback/)() const | Вызывается во время обработки источника шрифтов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
| [GetAvailableFonts](./getavailablefonts/)() | Возвращает список шрифтов, доступных через этот источник. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Вызывается во время обработки источника шрифтов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
