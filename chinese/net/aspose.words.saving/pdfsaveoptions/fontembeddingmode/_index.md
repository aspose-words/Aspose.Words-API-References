---
title: PdfSaveOptions.FontEmbeddingMode
linktitle: FontEmbeddingMode
articleTitle: FontEmbeddingMode
second_title: Aspose.Words for .NET
description: 探索 PdfSaveOptions FontEmbeddingMode 属性，优化 PDF 的字体嵌入。轻松提升文档质量和兼容性！
type: docs
weight: 170
url: /zh/net/aspose.words.saving/pdfsaveoptions/fontembeddingmode/
---
## PdfSaveOptions.FontEmbeddingMode property

指定字体嵌入模式。

```csharp
public PdfFontEmbeddingMode FontEmbeddingMode { get; set; }
```

## 评论

默认值为EmbedAll。

此设置仅适用于 ANSI (Windows-1252) 编码的文本。如果文档包含 非 ANSI 文本，则无论此设置如何，都会嵌入相应的字体。

PDF/A 和 PDF/UA 合规性要求嵌入所有字体。 EmbedAll保存到 PDF/A 和 PDF/UA 时将自动使用该值。

## 例子

展示如何设置 Aspose.Words 以跳过将 Arial 和 Times New Roman 字体嵌入 PDF 文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// “Arial”是标准字体，“Courier New”是非标准字体。
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();
// 将“EmbedFullFonts”属性设置为“true”以在输出 PDF 中嵌入每个嵌入字体的每个字形。
options.EmbedFullFonts = true;
// 将“FontEmbeddingMode”属性设置为“EmbedAll”以在输出 PDF 中嵌入所有字体。
// 将“FontEmbeddingMode”属性设置为“EmbedNonstandard”以仅允许在输出 PDF 中嵌入非标准字体。
// 将“FontEmbeddingMode”属性设置为“EmbedNone”以不在输出 PDF 中嵌入任何字体。
options.FontEmbeddingMode = pdfFontEmbeddingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);
```

### 也可以看看

* enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
