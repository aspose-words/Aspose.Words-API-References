---
title: HtmlSaveOptions.Encoding
second_title: Aspose.Words for .NET API 参考
description: HtmlSaveOptions 财产. 指定导出为 HTMLMHTML 或 EPUB 时使用的编码 默认值为新的 UTF8 编码假UTF8 无 BOM.
type: docs
weight: 100
url: /zh/net/aspose.words.saving/htmlsaveoptions/encoding/
---
## HtmlSaveOptions.Encoding property

指定导出为 HTML、MHTML 或 EPUB 时使用的编码。 默认值为`新的 UTF8 编码（假）`（UTF-8 无 BOM）.

```csharp
public Encoding Encoding { get; set; }
```

### 例子

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

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../htmlsaveoptions/)
* 部件 [Aspose.Words](../../../)


