---
title: "Konstruktorn Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource"
linktitle: "MemoryFontSource"
second_title: "Aspose.Words för C++ API‑referens"
description: "Konstruktorn Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource. Konstruktor i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fonts/memoryfontsource/memoryfontsource/
---
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&) constructor


Konstruktör.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Binär teckensnittsdata. |

## Exempel



Visar hur man använder en bytearray med data från en teckensnittfil som en teckensnittskälla.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Se även

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t) constructor


Konstruktör.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Binär teckensnittsdata. |
| priority | int32_t | [Font](../../../aspose.words/font/) källprioritet. Se beskrivningen av egenskapen [Priority](../../fontsourcebase/get_priority/) för mer information. |

## Exempel



Visar hur man använder en bytearray med data från en teckensnittfil som en teckensnittskälla.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Se även

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) constructor


Konstruktör.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority, const System::String &cacheKey)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Binär teckensnittsdata. |
| priority | int32_t | [Font](../../../aspose.words/font/) källprioritet. Se beskrivningen av egenskapen [Priority](../../fontsourcebase/get_priority/) för mer information. |
| cacheKey | const System::String\& | Nyckeln för denna källa i cachen. Se [CacheKey](../get_cachekey/) egenskapsbeskrivning för mer information. |

## Se även

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
