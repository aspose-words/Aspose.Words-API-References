---
title: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings 方法"
linktitle: "LoadMsOfficeFallbackSettings"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings 方法。加载预定义的回退设置，模拟 Microsoft Word 的回退并在 C++ 中使用 Microsoft Office 字体。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings::LoadMsOfficeFallbackSettings method


加载预定义的回退设置，该设置模拟 Microsoft Word 的回退并使用 Microsoft Office 字体。

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings()
```


## 示例



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
