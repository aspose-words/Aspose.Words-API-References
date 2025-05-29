---
title: FontFallbackSettings.LoadMsOfficeFallbackSettings
linktitle: LoadMsOfficeFallbackSettings
articleTitle: LoadMsOfficeFallbackSettings
second_title: Aspose.Words for .NET
description: 探索 FontFallbackSettings LoadMsOfficeFallbackSettings 方法，轻松实现类似 Microsoft Word 的后备设置与 Office 字体的无缝集成。
type: docs
weight: 30
url: /zh/net/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings.LoadMsOfficeFallbackSettings method

加载预定义的后备设置，模仿 Microsoft Word 后备并使用 Microsoft Office 字体。

```csharp
public void LoadMsOfficeFallbackSettings()
```

## 例子

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
