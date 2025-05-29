---
title: SaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words for .NET
description: 了解如何使用 SaveOptions SaveFormat 属性轻松选择文档的保存格式，以实现最佳灵活性和控制力。
type: docs
weight: 130
url: /zh/net/aspose.words.saving/saveoptions/saveformat/
---
## SaveOptions.SaveFormat property

如果使用此保存选项对象，则指定将保存文档的格式。

```csharp
public abstract SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
