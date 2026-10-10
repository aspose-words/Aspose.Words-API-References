---
title: "Costruttore MemoryFontSource di Aspose::Words::Fonts::MemoryFontSource"
linktitle: "MemoryFontSource"
second_title: "Riferimento API Aspose.Words per C++"
description: "Costruttore MemoryFontSource di Aspose::Words::Fonts::MemoryFontSource. Costruttore in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fonts/memoryfontsource/memoryfontsource/
---
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&) constructor


Costruttore.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Dati binari del carattere. |

## Esempi



Mostra come utilizzare un array di byte con i dati di un file di carattere come sorgente di caratteri.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Vedi anche

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t) constructor


Costruttore.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Dati binari del carattere. |
| priority | int32_t | [Font](../../../aspose.words/font/) priorità della sorgente. Vedi la descrizione della proprietà [Priority](../../fontsourcebase/get_priority/) per ulteriori informazioni. |

## Esempi



Mostra come utilizzare un array di byte con i dati di un file di carattere come sorgente di caratteri.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Vedi anche

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) constructor


Costruttore.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority, const System::String &cacheKey)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Dati binari del carattere. |
| priority | int32_t | [Font](../../../aspose.words/font/) priorità della sorgente. Vedi la descrizione della proprietà [Priority](../../fontsourcebase/get_priority/) per ulteriori informazioni. |
| cacheKey | const System::String\& | La chiave di questa origine nella cache. Vedi la descrizione della proprietà [CacheKey](../get_cachekey/) per maggiori informazioni. |

## Vedi anche

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
