---
title: SaveOptions.SaveFormat
second_title: Aspose.Words for .NET API 参考
description: SaveOptions 财产. 指定使用此保存选项对象时文档的保存格式
type: docs
weight: 140
url: /zh/net/aspose.words.saving/saveoptions/saveformat/
---
## SaveOptions.SaveFormat property

指定使用此保存选项对象时文档的保存格式。

```csharp
public abstract SaveFormat SaveFormat { get; set; }
```

### 例子

显示将文档保存到 .epub 时如何使用特定编码。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 使用 SaveOptions 对象来指定我们要保存的文档的编码。
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// 默认情况下，输出的 .epub 文档将其所有内容都放在一个 HTML 部分中。
// 分割标准允许我们将文档分割成几个 HTML 部分。
// 我们将设置将文档拆分为标题段落的标准。
// 这对于无法阅读比特定大小更重要的 HTML 文件的读者很有用。
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// 指定我们要导出文档属性。
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../saveoptions/)
* 部件 [Aspose.Words](../../../)


