---
title: "Aspose::Words::Fonts::FileFontSource::FileFontSource 构造函数"
linktitle: "FileFontSource"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FileFontSource::FileFontSource 构造函数。C++ 中的构造函数。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fonts/filefontsource/filefontsource/
---
## FileFontSource::FileFontSource(const System::String\&) constructor


构造函数。

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| filePath | const System::String\& | 字体文件的路径。 |

## 示例



展示如何在本地文件系统中将字体文件用作字体来源。
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## 另见

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FileFontSource::FileFontSource(const System::String\&, int32_t) constructor


构造函数。

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath, int32_t priority)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| filePath | const System::String\& | 字体文件的路径。 |
| priority | int32_t | [Font](../../../aspose.words/font/) 源优先级。有关更多信息，请参阅 [Priority](../../fontsourcebase/get_priority/) 属性描述。 |

## 示例



展示如何在本地文件系统中将字体文件用作字体来源。
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## 另见

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FileFontSource::FileFontSource(const System::String\&, int32_t, const System::String\&) constructor


构造函数。

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath, int32_t priority, const System::String &cacheKey)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| filePath | const System::String\& | 字体文件的路径。 |
| priority | int32_t | [Font](../../../aspose.words/font/) 源优先级。有关更多信息，请参阅 [Priority](../../fontsourcebase/get_priority/) 属性描述。 |
| cacheKey | const System::String\& | 此来源在缓存中的键。有关更多信息，请参阅 [CacheKey](../get_cachekey/) 属性描述。 |

## 另见

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
