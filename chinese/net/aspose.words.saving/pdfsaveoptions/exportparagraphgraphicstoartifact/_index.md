---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
linktitle: ExportParagraphGraphicsToArtifact
articleTitle: ExportParagraphGraphicsToArtifact
second_title: 用于 .NET 的 Aspose.Words
description: PdfSaveOptions ExportParagraphGraphicsToArtifact 财产. 获取或设置一个值确定段落图形是否应标记为工件 在 C#.
type: docs
weight: 160
url: /zh/net/aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/
---
## PdfSaveOptions.ExportParagraphGraphicsToArtifact property

获取或设置一个值，确定段落图形是否应标记为工件。

```csharp
public bool ExportParagraphGraphicsToArtifact { get; set; }
```

## 评论

默认值为`错误的`而段落图形（下划线、文本强调等） 将在文档的逻辑结构中标记为“Span”。

当值为`真的`段落图形将被标记为“Artifact”。

当以下情况时该值被忽略[`ExportDocumentStructure`](../exportdocumentstructure/)是`错误的` 。

## 例子

演示如何将段落图形导出为工件（下划线、文本强调等）。

```csharp
Document doc = new Document(MyDir + "PDF artifacts.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.ExportDocumentStructure = true;
saveOptions.ExportParagraphGraphicsToArtifact = true;
saveOptions.TextCompression = PdfTextCompression.None;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportParagraphGraphicsToArtifact.pdf", saveOptions);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
