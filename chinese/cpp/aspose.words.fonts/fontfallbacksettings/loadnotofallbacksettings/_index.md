---
title: "Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings method"
linktitle: "LoadNotoFallbackSettings"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings 方法。加载使用 Google Noto 字体的预定义回退设置（C++）。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings::LoadNotoFallbackSettings method


加载使用 Google Noto 字体的预定义回退设置。

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings()
```


## 示例



展示如何为 Google Noto 字体添加预定义的字体回退设置。
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();

// 这些是基于 SIL 开放字体许可证的免费字体。
// 我们可以在此下载这些字体：
// https://www.google.com/get/noto/#sans-lgc
fontSettings->SetFontsFolder(get_FontsDir() + u"Noto", false);

// 请注意，预定义设置仅使用常规粗细的无衬线（Sans）风格 Noto 字体。
// 部分 Noto 字体使用高级排版特性。
// 由于 Aspose.Words 目前不支持高级排版，这些带有高级排版的字体可能无法正确渲染。
fontSettings->get_FallbackSettings()->LoadNotoFallbackSettings();
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(false);
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Noto Sans");

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(fontSettings);
```


展示如何加载预定义的回退字体设置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// 将默认的回退字体方案保存为 XML 文档。
// 例如，其中一个元素的 Range 值为 "0C00-0C7F"，对应的 FallbackFonts 值为 "Vani"。
// 这意味着如果文本使用的字体没有 0x0C00-0x0C7F Unicode 块的符号，
// 回退方案将使用 "Vani" 字体的符号作为替代。
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.Default.xml");

// 以下是我们可以选择的两种预定义字体回退方案。
// 1 - 使用默认的 Microsoft Office 方案，它与默认方案相同：
fontFallbackSettings->LoadMsOfficeFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 - 使用基于 Google Noto 字体构建的方案：
fontFallbackSettings->LoadNotoFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

## 另见

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
