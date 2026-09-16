---
title: "Aspose::Words::Fonts::DefaultFontSubstitutionRule 类"
linktitle: "DefaultFontSubstitutionRule"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::DefaultFontSubstitutionRule 类。默认字体替换规则。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class


默认字体替代规则。要了解更多信息，请访问 [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) 文档文章。

```cpp
class DefaultFontSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_DefaultFontName](./get_defaultfontname/)() | 获取或设置默认字体名称。 |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | 指定规则是否已启用。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DefaultFontName](./set_defaultfontname/)(const System::String\&) | 设置器用于 [Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName](./get_defaultfontname/)。 |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | 设置器用于 [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/)。 |
| static [Type](./type/)() |  |

## 示例



展示如何设置默认字体替换规则。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// 获取 FontSettings 中的默认替换规则。
// 此规则将把所有缺失的字体替换为"Times New Roman"。
System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> defaultFontSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution();
ASSERT_TRUE(defaultFontSubstitutionRule->get_Enabled());
ASSERT_EQ(u"Times New Roman", defaultFontSubstitutionRule->get_DefaultFontName());

// 将默认字体替代设置为"Courier New"。
defaultFontSubstitutionRule->set_DefaultFontName(u"Courier New");

// 使用文档生成器，添加一些使用我们未拥有的字体的文本，以观察替换的发生，
// 然后将结果渲染为 PDF。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Missing Font");
builder->Writeln(u"Line written in a missing font, which will be substituted with Courier New.");

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontSubstitutionRule.pdf");
```

## 另见

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
