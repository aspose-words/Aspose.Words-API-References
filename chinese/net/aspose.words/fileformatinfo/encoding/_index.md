---
title: FileFormatInfo.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words for .NET
description: 探索 FileFormatInfo 的 Encoding 属性，轻松识别文档编码。目前支持 HTML 格式，可获得精准的识别结果。
type: docs
weight: 10
url: /zh/net/aspose.words/fileformatinfo/encoding/
---
## FileFormatInfo.Encoding property

如果适用于当前文档格式，则获取检测到的编码。 目前仅检测 HTML 文档的编码。

```csharp
public Encoding Encoding { get; }
```

## 例子

展示如何检测 html 文件中的编码。

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// 仅当我们为 html 文档创建 FileFormatInfo 对象时才使用 Encoding 属性。
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### 也可以看看

* class [FileFormatInfo](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
