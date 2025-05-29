---
title: HtmlSaveOptions.DocumentSplitCriteria
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words for .NET
description: 探索 HtmlSaveOptions DocumentSplitCriteria 属性，优化 HTML、EPUB 和 AZW3 格式的文档保存。立即增强您的格式控制！
type: docs
weight: 80
url: /zh/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

指定保存文档时如何拆分Html , Epub或者Azw3格式. 默认为None对于 HTML and HeadingParagraph适用于 EPUB 和 AZW3。

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

## 评论

通常，您希望将文档作为单个文件保存为 HTML。 但在某些情况下，最好将输出拆分为几个较小的 HTML 页面。 保存为 HTML 格式时，这些页面将输出为单独的文件或流。 保存为 EPUB 格式时，它们将被合并到相应的包中。

以 MHTML 格式保存时无法拆分文档。

## 例子

展示如何在将文档保存为 .epub 时使用特定编码。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 使用 SaveOptions 对象指定我们将保存的文档的编码。
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// 默认情况下，输出的 .epub 文档的所有内容都包含在一个 HTML 部分中。
// 拆分标准允许我们将文档分成几个 HTML 部分。
// 我们将设置标准将文档拆分为标题段落。
// 这对于无法读取大于特定大小的 HTML 文件的读者很有用。
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// 指定我们想要导出文档属性。
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### 也可以看看

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
