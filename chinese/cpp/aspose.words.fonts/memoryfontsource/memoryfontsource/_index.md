---
title: "Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource 构造函数"
linktitle: "MemoryFontSource"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource 构造函数。C++ 中的构造函数。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fonts/memoryfontsource/memoryfontsource/
---
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&) constructor


构造函数。

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | 二进制字体数据。 |

## 示例



展示如何使用包含字体文件数据的字节数组作为字体源。
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## 另见

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t) constructor


构造函数。

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | 二进制字体数据。 |
| priority | int32_t | [Font](../../../aspose.words/font/) 源优先级。有关更多信息，请参阅 [Priority](../../fontsourcebase/get_priority/) 属性描述。 |

## 示例



展示如何使用包含字体文件数据的字节数组作为字体源。
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## 另见

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) constructor


构造函数。

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority, const System::String &cacheKey)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | 二进制字体数据。 |
| priority | int32_t | [Font](../../../aspose.words/font/) 源优先级。有关更多信息，请参阅 [Priority](../../fontsourcebase/get_priority/) 属性描述。 |
| cacheKey | const System::String\& | 此来源在缓存中的键。有关更多信息，请参阅 [CacheKey](../get_cachekey/) 属性描述。 |

## 另见

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
