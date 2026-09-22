---
title: "منشئ MemoryFontSource في Aspose::Words::Fonts::MemoryFontSource"
linktitle: "MemoryFontSource"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ MemoryFontSource في Aspose::Words::Fonts::MemoryFontSource. منشئ في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fonts/memoryfontsource/memoryfontsource/
---
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&) constructor


منشئ.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | بيانات الخط الثنائية. |

## أمثلة



يظهر كيفية استخدام مصفوفة بايت تحتوي على بيانات من ملف خط كمصدر للخط.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## انظر أيضًا

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t) constructor


منشئ.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | بيانات الخط الثنائية. |
| priority | int32_t | [Font](../../../aspose.words/font/) أولوية المصدر. راجع وصف خاصية [Priority](../../fontsourcebase/get_priority/) لمزيد من المعلومات. |

## أمثلة



يظهر كيفية استخدام مصفوفة بايت تحتوي على بيانات من ملف خط كمصدر للخط.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## انظر أيضًا

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) constructor


منشئ.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority, const System::String &cacheKey)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | بيانات الخط الثنائية. |
| priority | int32_t | [Font](../../../aspose.words/font/) أولوية المصدر. راجع وصف خاصية [Priority](../../fontsourcebase/get_priority/) لمزيد من المعلومات. |
| cacheKey | const System::String\& | مفتاح هذا المصدر في الذاكرة المؤقتة. راجع وصف خاصية [CacheKey](../get_cachekey/) لمزيد من المعلومات. |

## انظر أيضًا

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
