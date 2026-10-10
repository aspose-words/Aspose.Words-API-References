---
title: "Aspose::Words::Fonts::FileFontSource class"
linktitle: "FileFontSource"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FileFontSource class. 表示存储在文件系统中的单个 TrueType 字体文件。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fonts/filefontsource/
---
## FileFontSource class


表示存储在文件系统中的单个 TrueType 字体文件。要了解更多信息，请访问 [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) 文档文章。

```cpp
class FileFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [FileFontSource](./filefontsource/)(const System::String\&) | 构造函数。 |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t) | 构造函数。 |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t, const System::String\&) | 构造函数。 |
| [get_CacheKey](./get_cachekey/)() const | 此来源在缓存中的键。 |
| [get_FilePath](./get_filepath/)() const | 字体文件的路径。 |
| [get_Priority](../fontsourcebase/get_priority/)() const | 返回字体源的优先级。 |
| [get_Type](./get_type/)() override | 返回字体源的类型。 |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | 在处理字体源时调用，如果检测到可能导致格式保真度损失的问题。 |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | 返回通过此源可用的字体列表。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | 在处理字体源时调用，如果检测到可能导致格式保真度损失的问题。 |
| static [Type](./type/)() |  |

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

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
