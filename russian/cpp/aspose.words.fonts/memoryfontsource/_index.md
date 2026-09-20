---
title: "Aspose::Words::Fonts::MemoryFontSource class"
linktitle: "MemoryFontSource"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::MemoryFontSource class. Представляет единственный файл шрифта TrueType, хранящийся в памяти. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class


Представляет отдельный файл TrueType, хранящийся в памяти. Чтобы узнать больше, посетите статью документации [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class MemoryFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | Ключ этого источника в кэше. |
| [get_FontData](./get_fontdata/)() const | Бинарные данные шрифта. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Возвращает приоритет источника шрифтов. |
| [get_Type](./get_type/)() override | Возвращает тип источника шрифтов. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Вызывается во время обработки источника шрифтов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Возвращает список шрифтов, доступных через этот источник. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&) | Конструктор. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t) | Конструктор. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) | Конструктор. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Вызывается во время обработки источника шрифтов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как использовать массив байтов с данными из файла шрифта в качестве источника шрифта.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## См. также

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
