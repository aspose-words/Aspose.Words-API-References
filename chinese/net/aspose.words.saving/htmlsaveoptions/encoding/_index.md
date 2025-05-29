---
title: HtmlSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words for .NET
description: 探索 HtmlSaveOptions 编码，实现无缝 HTML、MHTML 和 EPUB 导出。轻松使用 UTF-8 自定义编码，实现最佳兼容性和性能。
type: docs
weight: 100
url: /zh/net/aspose.words.saving/htmlsaveoptions/encoding/
---
## HtmlSaveOptions.Encoding property

指定导出为 HTML、MHTML 或 EPUB 时使用的编码。 默认值为`新的 UTF8Encoding（false）`（无 BOM 的 UTF-8）.

```csharp
public Encoding Encoding { get; set; }
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

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
