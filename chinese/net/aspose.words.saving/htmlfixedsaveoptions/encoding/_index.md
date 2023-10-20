---
title: HtmlFixedSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: 用于 .NET 的 Aspose.Words
description: HtmlFixedSaveOptions Encoding 财产. 指定导出为 HTML 时使用的编码 默认值为新的UTF8编码真带 BOM 的 UTF8 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

指定导出为 HTML 时使用的编码。 默认值为`新的UTF8编码（真）`（带 BOM 的 UTF-8）.

```csharp
public Encoding Encoding { get; set; }
```

## 例子

演示如何设置将文档导出为 HTML 时使用的编码。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

// 默认编码为UTF-8。如果我们想使用不同的编码来表示我们的文档，
// 我们可以使用 SaveOptions 对象来设置特定的编码。
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.GetEncoding("ASCII")
};

Assert.AreEqual("US-ASCII", htmlFixedSaveOptions.Encoding.EncodingName);

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### 也可以看看

* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
