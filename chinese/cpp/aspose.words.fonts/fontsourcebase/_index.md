---
title: "Aspose::Words::Fonts::FontSourceBase 类"
linktitle: "FontSourceBase"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontSourceBase 类。这是一个抽象基类，用于允许用户指定各种字体源的类。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class


这是一个抽象基类，供允许用户指定各种字体来源的类使用。欲了解更多，请访问[Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/)文档文章。

```cpp
class FontSourceBase : public Aspose::Fonts::IFontSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Priority](./get_priority/)() const | 返回字体源的优先级。 |
| virtual [get_Type](./get_type/)() | 返回字体源的类型。 |
| [get_WarningCallback](./get_warningcallback/)() const | 在处理字体源时调用，如果检测到可能导致格式保真度损失的问题。 |
| [GetAvailableFonts](./getavailablefonts/)() | 返回通过此源可用的字体列表。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | 在处理字体源时调用，如果检测到可能导致格式保真度损失的问题。 |
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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
