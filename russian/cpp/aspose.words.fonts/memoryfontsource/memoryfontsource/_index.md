---
title: "Конструктор MemoryFontSource класса Aspose::Words::Fonts::MemoryFontSource"
linktitle: "MemoryFontSource"
second_title: "Справочник API Aspose.Words для C++"
description: "Конструктор MemoryFontSource класса Aspose::Words::Fonts::MemoryFontSource. Конструктор в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fonts/memoryfontsource/memoryfontsource/
---
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&) constructor


Конструктор.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Бинарные данные шрифта. |

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

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t) constructor


Конструктор.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Бинарные данные шрифта. |
| priority | int32_t | [Font](../../../aspose.words/font/) приоритет источника. Смотрите описание свойства [Priority](../../fontsourcebase/get_priority/) для получения дополнительной информации. |

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

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) constructor


Конструктор.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority, const System::String &cacheKey)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Бинарные данные шрифта. |
| priority | int32_t | [Font](../../../aspose.words/font/) приоритет источника. Смотрите описание свойства [Priority](../../fontsourcebase/get_priority/) для получения дополнительной информации. |
| cacheKey | const System::String\& | Ключ этого источника в кэше. См. описание свойства [CacheKey](../get_cachekey/) для получения дополнительной информации. |

## См. также

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
