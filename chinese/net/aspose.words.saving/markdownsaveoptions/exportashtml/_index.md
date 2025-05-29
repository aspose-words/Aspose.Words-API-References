---
title: MarkdownSaveOptions.ExportAsHtml
linktitle: ExportAsHtml
articleTitle: ExportAsHtml
second_title: Aspose.Words for .NET
description: 了解 MarkdownSaveOptions ExportAsHtml 属性如何让您自定义 HTML 元素，从而实现无缝 Markdown 导出。最大限度地提升内容的多功能性！
type: docs
weight: 30
url: /zh/net/aspose.words.saving/markdownsaveoptions/exportashtml/
---
## MarkdownSaveOptions.ExportAsHtml property

允许指定要作为原始 HTML 导出到 Markdown 的元素。 默认值为None.

```csharp
public MarkdownExportAsHtml ExportAsHtml { get; set; }
```

## 例子

展示如何将表格作为原始 HTML 导出到 Markdown。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Sample table:");

// 创建表。
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;
builder.Write("Cell1");
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write("Cell2");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ExportAsHtml = MarkdownExportAsHtml.Tables;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

### 也可以看看

* enum [MarkdownExportAsHtml](../../markdownexportashtml/)
* class [MarkdownSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
