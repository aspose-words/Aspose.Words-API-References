---
title: HtmlSaveOptions.DocumentSplitCriteria
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: 用于 .NET 的 Aspose.Words
description: HtmlSaveOptions DocumentSplitCriteria 财产. 指定保存时文档应如何分割Html Epub或者Azw3格式 默认为None对于 HTML 和 HeadingParagraph适用于 EPUB 和 AZW3 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

指定保存时文档应如何分割Html, Epub或者Azw3格式。 默认为None对于 HTML 和 HeadingParagraph适用于 EPUB 和 AZW3.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

## 评论

通常您希望将文档保存为 HTML 作为单个文件。 但在某些情况下，最好将输出分割成几个较小的 HTML 页面。 保存为 HTML 格式时，这些页面将输出到单独的文件或流中。 保存为 EPUB 格式时，它们将被合并到相应的包中。

以 MHTML 格式保存时无法分割文档。

## 例子

演示将文档保存为 .epub 时如何使用特定编码。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 使用 SaveOptions 对象指定我们将保存的文档的编码。
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// 默认情况下，输出 .epub 文档的所有内容都位于一个 HTML 部分中。
// 分割标准允许我们将文档分割成几个 HTML 部分。
// 我们将设置将文档拆分为标题段落的标准。
// 这对于无法读取大于特定大小的 HTML 文件的读者很有用。
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// 指定我们要导出文档属性。
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### 也可以看看

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
