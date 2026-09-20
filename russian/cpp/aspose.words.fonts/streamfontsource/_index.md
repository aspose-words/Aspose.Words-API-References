---
title: "Aspose::Words::Fonts::StreamFontSource class"
linktitle: "StreamFontSource"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::StreamFontSource class. Базовый класс для пользовательского источника шрифта из потока. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class


Базовый класс для пользовательского потокового источника шрифтов. Чтобы узнать больше, посетите статью документации [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class StreamFontSource : public Aspose::Words::Fonts::FontSourceBase,
                         public Aspose::Fonts::IFontData
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | Ключ этого источника в кэше. |
| [get_IsEmbedded](./get_isembedded/)() override |  |
| [get_Priority](../fontsourcebase/get_priority/)() const | Возвращает приоритет источника шрифтов. |
| [get_Type](./get_type/)() override | Возвращает тип источника шрифтов. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Вызывается во время обработки источника шрифтов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Возвращает список шрифтов, доступных через этот источник. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [OpenFontDataStream](./openfontdatastream/)() | Этот метод должен открывать поток с данными шрифта по требованию. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Вызывается во время обработки источника шрифтов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
| static [Type](./type/)() |  |
## Примечания


Чтобы использовать источник шрифтов из потока, вам следует создать производный класс от [StreamFontSource](./) и предоставить реализацию метода [OpenFontDataStream](./openfontdatastream/).

[OpenFontDataStream](./openfontdatastream/) method could be called several times. For the first time it will be called when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](./) may be useful because it allows to load the font data only when it is required and not to store it in the memory for the [FontSettings](../fontsettings/) lifetime. 
## См. также

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
