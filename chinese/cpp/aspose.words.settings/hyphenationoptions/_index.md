---
title: "Aspose::Words::Settings::HyphenationOptions 类"
linktitle: "HyphenationOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::HyphenationOptions 类。允许配置文档连字选项。要了解更多，请访问 C++ 中的文档文章。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class


允许配置文档连字符选项。欲了解更多，请访问 [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/) 文档文章。

```cpp
class HyphenationOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_AutoHyphenation](./get_autohyphenation/)() const | 获取或设置决定文档是否启用自动连字的值。此属性的默认值为 **false**。 |
| [get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/)() const | 获取或设置可以以连字符结尾的连续行的最大数量。此属性的默认值为 0。 |
| [get_HyphenateCaps](./get_hyphenatecaps/)() const | 获取或设置决定全大写单词是否进行连字的值。此属性的默认值为 **true**。 |
| [get_HyphenationZone](./get_hyphenationzone/)() const | 获取或设置从右边距起的距离（以 1/20 点为单位），在此范围内不进行连字。此属性的默认值为 360（0.25 英寸）。 |
| [GetType](./gettype/)() const override |  |
| [HyphenationOptions](./hyphenationoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AutoHyphenation](./set_autohyphenation/)(bool) | 用于设置 [Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation](./get_autohyphenation/)。 |
| [set_ConsecutiveHyphenLimit](./set_consecutivehyphenlimit/)(int32_t) | 用于设置 [Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/)。 |
| [set_HyphenateCaps](./set_hyphenatecaps/)(bool) | 用于设置 [Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps](./get_hyphenatecaps/)。 |
| [set_HyphenationZone](./set_hyphenationzone/)(int32_t) | 用于设置 [Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone](./get_hyphenationzone/)。 |
| static [Type](./type/)() |  |

## 示例



展示如何配置自动连字。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(24);
builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->get_HyphenationOptions()->set_AutoHyphenation(true);
doc->get_HyphenationOptions()->set_ConsecutiveHyphenLimit(2);
doc->get_HyphenationOptions()->set_HyphenationZone(720);
doc->get_HyphenationOptions()->set_HyphenateCaps(true);

doc->Save(get_ArtifactsDir() + u"Document.HyphenationOptions.docx");
```

## 另见

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
