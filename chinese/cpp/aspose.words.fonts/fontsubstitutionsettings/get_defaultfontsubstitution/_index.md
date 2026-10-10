---
title: "Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution 方法"
linktitle: "get_DefaultFontSubstitution"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution 方法。与 C++ 中默认字体替代规则相关的设置。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fonts/fontsubstitutionsettings/get_defaultfontsubstitution/
---
## FontSubstitutionSettings::get_DefaultFontSubstitution method


[Settings](../../../aspose.words.settings/) related to default font substitution rule.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> & Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution() const
```


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

* Class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* Class [FontSubstitutionSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
