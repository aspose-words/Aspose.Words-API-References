---
title: FileFormatInfo.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: 用于 .NET 的 Aspose.Words
description: FileFormatInfo Encoding 财产. 获取检测到的编码如果适用于当前文档格式 目前仅检测 HTML 文档的编码 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words/fileformatinfo/encoding/
---
## FileFormatInfo.Encoding property

获取检测到的编码（如果适用于当前文档格式）。 目前仅检测 HTML 文档的编码。

```csharp
public Encoding Encoding { get; }
```

## 例子

演示如何检测 html 文件中的编码。

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// Encoding 属性仅在我们为 html 文档创建 FileFormatInfo 对象时使用。
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### 也可以看看

* class [FileFormatInfo](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
