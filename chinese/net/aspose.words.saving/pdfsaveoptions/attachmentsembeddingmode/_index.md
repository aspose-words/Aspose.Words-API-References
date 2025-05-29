---
title: PdfSaveOptions.AttachmentsEmbeddingMode
linktitle: AttachmentsEmbeddingMode
articleTitle: AttachmentsEmbeddingMode
second_title: Aspose.Words for .NET
description: 使用 PdfSaveOptions 自定义附件在 PDF 中的嵌入方式。确保无缝集成并优化文档共享。
type: docs
weight: 30
url: /zh/net/aspose.words.saving/pdfsaveoptions/attachmentsembeddingmode/
---
## PdfSaveOptions.AttachmentsEmbeddingMode property

获取或设置一个值，确定附件如何嵌入到 PDF 文档中。

```csharp
public PdfAttachmentsEmbeddingMode AttachmentsEmbeddingMode { get; set; }
```

## 评论

默认值为None并且未嵌入附件。

PDF/A-1、PDF/A-2 和常规 PDF/A-4（非 PDF/A-4f）标准不允许嵌入文件。 None值将自动使用。

## 例子

展示如何将嵌入附件添加到 PDF 文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.AttachmentsEmbeddingMode = PdfAttachmentsEmbeddingMode.Annotations;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", saveOptions);
```

### 也可以看看

* enum [PdfAttachmentsEmbeddingMode](../../pdfattachmentsembeddingmode/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
