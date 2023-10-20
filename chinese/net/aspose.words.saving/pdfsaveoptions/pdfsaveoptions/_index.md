---
title: PdfSaveOptions
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: 用于 .NET 的 Aspose.Words
description: PdfSaveOptions 构造函数. 初始化此类的新实例该实例可用于在 中保存文档Pdf格式 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.saving/pdfsaveoptions/pdfsaveoptions/
---
## PdfSaveOptions constructor

初始化此类的新实例，该实例可用于在 中保存文档Pdf格式.

```csharp
public PdfSaveOptions()
```

## 例子

演示如何在将文档渲染为 PDF 时嵌入字体时启用或禁用子集化。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// 配置我们的字体源以确保我们可以访问本文档中的两种字体。
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource = new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 由于我们的文档包含自定义字体，因此可能需要嵌入到输出文档中。
// 将“EmbedFullFonts”属性设置为“true”以在输出 PDF 中嵌入每个嵌入字体的每个字形。
// 文档的大小可能会变得很大，但是如果我们编辑PDF，我们将充分利用所有字体。
// 将“EmbedFullFonts”属性设置为“false”以对字体应用子集化，仅保存字形
// 该文档正在使用。文件将会小得多，
// 但如果我们编辑文档，我们可能需要访问任何自定义字体。
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

if (embedFullFonts)
    Assert.That(500000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf").Length));
else
    Assert.That(25000, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf").Length));

// 恢复原始字体源。
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
