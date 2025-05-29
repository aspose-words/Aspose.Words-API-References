---
title: PdfSaveOptions.UseCoreFonts
linktitle: UseCoreFonts
articleTitle: UseCoreFonts
second_title: Aspose.Words for .NET
description: 使用 PdfSaveOptions 优化您的 PDF！控制 Arial 和 Times New Roman 等 TrueType 字体的替换，以提升文档质量。
type: docs
weight: 330
url: /zh/net/aspose.words.saving/pdfsaveoptions/usecorefonts/
---
## PdfSaveOptions.UseCoreFonts property

获取或设置一个值，确定是否用核心 PDF Type 1 字体替换 TrueType 字体 Arial、Times New Roman、 Courier New 和 Symbol。

```csharp
public bool UseCoreFonts { get; set; }
```

## 评论

默认值为`错误的` 。当此值设置为`真的`PDF 文档中的 Arial、Times New Roman、 Courier New 和 Symbol 字体被相应的核心 Type 1 字体替换。

any PDF 查看器应用程序必须能够使用核心 PDF 字体或其字体规格和合适的替代字体。

此设置仅适用于 ANSI (Windows-1252) 编码的文本。无论此设置如何，非 ANSI 文本都将以嵌入 TrueType 字体的形式写入 。

PDF/A 和 PDF/UA 合规性要求嵌入所有字体。`错误的`保存为 PDF/A 和 PDF/UA 时，值将自动使用 。

保存为 PDF 2.0 格式时不支持核心字体。`错误的`保存为 PDF 2.0 时将自动使用 值。

该选项的优先级高于[`FontEmbeddingMode`](../fontembeddingmode/)选项。

## 例子

显示如何启用/禁用 PDF Type 1 字体替换。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();
// 将“UseCoreFonts”属性设置为“true”以替换某些字体，
// 在我们的文档中包含这两种字体，以及它们的 PDF Type 1 等效字体。
// 将“UseCoreFonts”属性设置为“false”以不应用 PDF Type 1 字体。
options.UseCoreFonts = useCoreFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf", options);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
