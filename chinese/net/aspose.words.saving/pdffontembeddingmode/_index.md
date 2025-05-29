---
title: PdfFontEmbeddingMode Enum
linktitle: PdfFontEmbeddingMode
articleTitle: PdfFontEmbeddingMode
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.PdfFontEmbeddingMode 枚举，实现 PDF 中最佳的字体嵌入。提升文档质量并确保文本显示的一致性。
type: docs
weight: 6260
url: /zh/net/aspose.words.saving/pdffontembeddingmode/
---
## PdfFontEmbeddingMode enumeration

指定 Aspose.Words 如何嵌入字体。

```csharp
public enum PdfFontEmbeddingMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| EmbedAll | `0` | Aspose.Words 嵌入所有字体。 |
| EmbedNonstandard | `1` | Aspose.Words 嵌入除标准 Windows 字体 Arial 和 Times New Roman 之外的所有字体。 在此模式下，只有 Arial 和 Times New Roman 字体会受到影响，因为 MS Word 在将文档保存为 PDF 时不会嵌入 仅这些字体。 |
| EmbedNone | `2` | Aspose.Words 不嵌入任何字体。 |

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

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
