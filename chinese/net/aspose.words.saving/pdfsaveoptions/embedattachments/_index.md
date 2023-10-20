---
title: PdfSaveOptions.EmbedAttachments
linktitle: EmbedAttachments
articleTitle: EmbedAttachments
second_title: 用于 .NET 的 Aspose.Words
description: PdfSaveOptions EmbedAttachments 财产. 获取或设置一个值确定是否将附件嵌入到 PDF 文档中 在 C#.
type: docs
weight: 110
url: /zh/net/aspose.words.saving/pdfsaveoptions/embedattachments/
---
## PdfSaveOptions.EmbedAttachments property

获取或设置一个值，确定是否将附件嵌入到 PDF 文档中。

```csharp
public bool EmbedAttachments { get; set; }
```

## 评论

默认值为`错误的`并且附件未嵌入。

当值为`真的`附件嵌入到 PDF 文档中。

保存为 PDF/A 和 PDF/UA 合规性时不支持嵌入附件。 `错误的`值将被自动使用。

启用加密时不支持嵌入附件。`错误的` value 将被自动使用。

## 例子

演示如何将嵌入附件添加到 PDF 文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions options = new PdfSaveOptions();
options.EmbedAttachments = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", options);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
