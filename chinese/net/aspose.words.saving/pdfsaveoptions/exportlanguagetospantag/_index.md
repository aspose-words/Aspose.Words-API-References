---
title: PdfSaveOptions.ExportLanguageToSpanTag
second_title: Aspose.Words for .NET API 参考
description: PdfSaveOptions 财产. 获取或设置一个值确定是否在文档结构中创建Span标签以导出文本语言
type: docs
weight: 150
url: /zh/net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## PdfSaveOptions.ExportLanguageToSpanTag property

获取或设置一个值，确定是否在文档结构中创建“Span”标签以导出文本语言。

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

### 评论

默认值为`错误的`“Lang”属性被附加到页面内容流中的标记内容序列。

当值为`真的`为具有非默认 language 的文本创建“Span”标签，并将“Lang”属性附加到该标签。

当以下情况时该值被忽略[`ExportDocumentStructure`](../exportdocumentstructure/)是`错误的` 。

### 例子

演示如何在文档结构中创建“Span”标签以导出文本语言。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hola mundo!");

PdfSaveOptions saveOptions = new PdfSaveOptions
{
    // 请注意，当“ExportDocumentStructure”为 false 时，“ExportLanguageToSpanTag”将被忽略。
    ExportDocumentStructure = true, ExportLanguageToSpanTag = true
};

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../pdfsaveoptions/)
* 部件 [Aspose.Words](../../../)


