---
title: PdfSaveOptions.EmbedFullFonts
linktitle: EmbedFullFonts
articleTitle: EmbedFullFonts
second_title: Aspose.Words for .NET
description: 了解 PdfSaveOptions EmbedFullFonts 功能如何通过确保完整的字体嵌入以实现完美的格式来增强您的 PDF 文档。
type: docs
weight: 120
url: /zh/net/aspose.words.saving/pdfsaveoptions/embedfullfonts/
---
## PdfSaveOptions.EmbedFullFonts property

控制如何将字体嵌入到生成的 PDF 文档中。

```csharp
public bool EmbedFullFonts { get; set; }
```

## 评论

默认值为`错误的`，这意味着字体在嵌入之前会被子集化。 如果您想保持输出文件较小，子集化非常有用。子集化会从字体中删除所有 未使用的字形。

当此值设置为`真的`，将完整的字体文件嵌入到 PDF 中，无需进行子集设置。这会导致输出文件较大，但当您稍后想要编辑生成的 PDF（例如添加更多文本）时，这是一个非常有用的选项。

有些字体很大（几兆字节），如果不使用 subsetting 嵌入它们，将导致输出文档很大。

## 例子

展示如何在将文档呈现为 PDF 时启用或禁用嵌入字体的子集。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// 配置我们的字体源以确保我们可以访问此文档中的两种字体。
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource =
    new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 由于我们的文档包含自定义字体，因此可能需要嵌入到输出文档中。
// 将“EmbedFullFonts”属性设置为“true”以在输出 PDF 中嵌入每个嵌入字体的每个字形。
// 文档的大小可能会变得非常大，但如果我们编辑 PDF，我们将充分利用所有字体。
// 将“EmbedFullFonts”属性设置为“false”以将子集应用于字体，仅保存字形
// 文档正在使用。文件将会小得多，
// 但如果我们编辑文档，我们可能需要访问任何自定义字体。
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

// 恢复原始字体源。
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
