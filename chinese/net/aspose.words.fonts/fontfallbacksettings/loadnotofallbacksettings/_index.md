---
title: FontFallbackSettings.LoadNotoFallbackSettings
linktitle: LoadNotoFallbackSettings
articleTitle: LoadNotoFallbackSettings
second_title: Aspose.Words for .NET
description: 了解如何使用 FontFallbackSettings LoadNotoFallbackSettings 方法增强您的排版，并使用 Google Noto 字体实现无缝文本显示。
type: docs
weight: 40
url: /zh/net/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings.LoadNotoFallbackSettings method

加载使用 Google Noto 字体的预定义后备设置。

```csharp
public void LoadNotoFallbackSettings()
```

## 例子

展示如何为 Google Noto 字体添加预定义字体后备设置。

```csharp
FontSettings fontSettings = new FontSettings();

// 这些是根据 SIL 开放字体许可证授权的免费字体。
// 我们可以在这里下载字体：
// https://www.google.com/get/noto/#sans-lgc
fontSettings.SetFontsFolder(FontsDir + "Noto", false);

 // 请注意，预定义设置仅使用常规粗细的 Sans 风格 Noto 字体。
// 一些 Noto 字体使用高级排版功能。
// 由于 Aspose.Words 目前不支持高级排版字体，因此可能无法正确呈现它们。
fontSettings.FallbackSettings.LoadNotoFallbackSettings();
fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = false;
fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Noto Sans";

Document doc = new Document();
doc.FontSettings = fontSettings;
```

展示如何加载预定义的后备字体设置。

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// 将默认后备字体方案保存到 XML 文档。
// 例如，其中一个元素的 Range 值为“0C00-0C7F”，FallbackFonts 值为相应的“Vani”。
// 这意味着如果某些文本使用的字体没有 0x0C00-0x0C7F Unicode 块的符号，
// 后备方案将使用“Vani”字体替代中的符号。
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.Default.xml");

// 下面是两个预定义的字体后备方案供我们选择。
// 1 - 使用默认的 Microsoft Office 方案，与默认方案相同：
fontFallbackSettings.LoadMsOfficeFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 - 使用由 Google Noto 字体构建的方案：
fontFallbackSettings.LoadNotoFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

### 也可以看看

* class [FontFallbackSettings](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
