---
title: HtmlFixedSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words for .NET
description: 探索 HtmlFixedSaveOptions 编码属性，实现无缝 HTML 导出。轻松设置带 BOM 的 UTF-8 编码，实现最佳数据完整性。
type: docs
weight: 30
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

指定导出为 HTML 时使用的编码。 默认值为`新的 UTF8Encoding（true）`（带 BOM 的 UTF-8）.

```csharp
public Encoding Encoding { get; set; }
```

## 例子

展示如何设置将文档导出为 HTML 时使用的编码。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

// 默认编码是 UTF-8。如果我们想使用其他编码来表示文档，
// 我们可以使用 SaveOptions 对象来设置特定的编码。
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.ASCII
};

Assert.AreEqual("US-ASCII", htmlFixedSaveOptions.Encoding.EncodingName);

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### 也可以看看

* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
