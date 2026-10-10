---
title: "Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource Konstruktor"
linktitle: "MemoryFontSource"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource Konstruktor. Ctor in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fonts/memoryfontsource/memoryfontsource/
---
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&) constructor


Konstruktor.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Binäre Schriftartdaten. |

## Beispiele



Zeigt, wie man ein Byte-Array mit Daten aus einer Schriftdatei als Schriftquelle verwendet.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Siehe auch

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t) constructor


Konstruktor.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Binäre Schriftartdaten. |
| priority | int32_t | [Font](../../../aspose.words/font/) Quellpriorität. Siehe die [Priority](../../fontsourcebase/get_priority/) Eigenschaftsbeschreibung für weitere Informationen. |

## Beispiele



Zeigt, wie man ein Byte-Array mit Daten aus einer Schriftdatei als Schriftquelle verwendet.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Siehe auch

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) constructor


Konstruktor.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority, const System::String &cacheKey)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Binäre Schriftartdaten. |
| priority | int32_t | [Font](../../../aspose.words/font/) Quellpriorität. Siehe die [Priority](../../fontsourcebase/get_priority/) Eigenschaftsbeschreibung für weitere Informationen. |
| cacheKey | const System::String\& | Der Schlüssel dieser Quelle im Cache. Siehe die Beschreibung der Eigenschaft [CacheKey](../get_cachekey/) für weitere Informationen. |

## Siehe auch

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
