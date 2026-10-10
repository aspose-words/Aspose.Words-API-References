---
title: "Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource constructor"
linktitle: "MemoryFontSource"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource constructor. C++'ta yapıcı."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fonts/memoryfontsource/memoryfontsource/
---
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&) constructor


Yapıcı.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | İkili yazı tipi verileri. |

## Örnekler



Bir yazı tipi dosyasından gelen verilerle bir bayt dizisini yazı tipi kaynağı olarak nasıl kullanacağınızı gösterir.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Ayrıca Bakınız

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t) constructor


Yapıcı.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | İkili yazı tipi verileri. |
| priority | int32_t | [Font](../../../aspose.words/font/) kaynağı önceliği. Daha fazla bilgi için [Priority](../../fontsourcebase/get_priority/) özelliği açıklamasına bakın. |

## Örnekler



Bir yazı tipi dosyasından gelen verilerle bir bayt dizisini yazı tipi kaynağı olarak nasıl kullanacağınızı gösterir.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Ayrıca Bakınız

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) constructor


Yapıcı.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority, const System::String &cacheKey)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | İkili yazı tipi verileri. |
| priority | int32_t | [Font](../../../aspose.words/font/) kaynağı önceliği. Daha fazla bilgi için [Priority](../../fontsourcebase/get_priority/) özelliği açıklamasına bakın. |
| cacheKey | const System::String\& | Bu kaynağın önbellekteki anahtarı. Daha fazla bilgi için [CacheKey](../get_cachekey/) özelliği açıklamasına bakın. |

## Ayrıca Bakınız

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
