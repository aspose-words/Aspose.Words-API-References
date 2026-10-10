---
title: "Aspose::Words::Document::get_FontSettings 方法"
linktitle: "get_FontSettings"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_FontSettings 方法。获取或设置文档的字体设置（在 C++ 中）。"
type: docs
weight: 25000
url: /zh/cpp/aspose.words/document/get_fontsettings/
---
## Document::get_FontSettings method


获取或设置文档字体设置。

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Document::get_FontSettings() const
```

## 备注


此属性允许为每个文档指定字体设置。如果设置为 **null**，将使用默认的静态字体设置 [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/)。

默认值是 **null**。

## 示例



展示如何设置字体替换规则。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// 默认的字体来源包含文档使用的第一种字体。
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// 第二种字体 "Amethysta" 不可用。
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// 我们可以配置一个字体替换表，用于确定
// Aspose.Words 将使用哪些字体来替代不可用的字体。
// 为 "Amethysta" 设置两个替代字体："Arvo", 和 "Courier New"。
// 如果第一个替代字体不可用，Aspose.Words 将尝试使用第二个替代字体，依此类推。
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->SetSubstitutes(u"Amethysta", System::MakeArray<System::String>({u"Arvo", u"Courier New"}));

// "Amethysta" 不可用，替换规则指出第一个使用的替代字体是 "Arvo"。
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// "Arvo" 也不可用，但 "Courier New" 可用。
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// 输出文档将显示使用 "Amethysta" 字体的文本，但会以 "Courier New" 格式呈现。
doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitution.pdf");
```

## 另见

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
