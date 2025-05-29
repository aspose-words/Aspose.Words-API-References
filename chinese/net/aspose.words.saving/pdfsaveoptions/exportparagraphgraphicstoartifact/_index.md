---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
linktitle: ExportParagraphGraphicsToArtifact
articleTitle: ExportParagraphGraphicsToArtifact
second_title: Aspose.Words for .NET
description: 发现 PdfSaveOptions ExportParagraphGraphicsToArtifact 属性以将段落图形控制为工件，从而增强文档的视觉清晰度。
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

默认值为`错误的`并且段落图形（下划线、文本强调等） 将在文档的逻辑结构中被标记为“Span”。

当值为`真的`该段落图形将被标记为“Artifact”。

当发生以下情况时，此值将被忽略[`ExportDocumentStructure`](../exportdocumentstructure/)是`错误的` 。

## 例子

展示如何将段落图形导出为工件（下划线、文本强调等）。

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
