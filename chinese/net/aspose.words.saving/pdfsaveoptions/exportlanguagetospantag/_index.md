---
title: PdfSaveOptions.ExportLanguageToSpanTag
linktitle: ExportLanguageToSpanTag
articleTitle: ExportLanguageToSpanTag
second_title: Aspose.Words for .NET
description: 探索 PdfSaveOptions 的 ExportLanguageToSpanTag 属性。使用 Span 标签控制文本语言的导出，以增强文档结构和可访问性。
type: docs
weight: 150
url: /zh/net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## PdfSaveOptions.ExportLanguageToSpanTag property

获取或设置一个值，确定是否在文档结构中创建“Span”标签来导出文本语言。

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

## 评论

默认值为`错误的`并且“Lang”属性附加到页面内容流中的标记内容序列。

当值为`真的`为非默认语言 的文本创建“Span”标签，并将“Lang”属性附加到此标签。

当发生以下情况时，此值将被忽略[`ExportDocumentStructure`](../exportdocumentstructure/)是`错误的` 。

## 例子

展示如何在文档结构中创建“Span”标签来导出文本语言。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hola mundo!");

PdfSaveOptions saveOptions = new PdfSaveOptions
{
    // 注意，当“ExportDocumentStructure”为假时，“ExportLanguageToSpanTag”将被忽略。
    ExportDocumentStructure = true, ExportLanguageToSpanTag = true
};

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
