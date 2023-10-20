---
title: CustomXmlPart.DataChecksum
linktitle: DataChecksum
articleTitle: DataChecksum
second_title: 用于 .NET 的 Aspose.Words
description: CustomXmlPart DataChecksum 财产. 指定循环冗余校验 CRC 校验和Data内容 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.markup/customxmlpart/datachecksum/
---
## CustomXmlPart.DataChecksum property

指定循环冗余校验 (CRC) 校验和[`Data`](../data/)内容.

```csharp
public long DataChecksum { get; }
```

## 例子

显示如何在运行时计算校验和。

```csharp
Document doc = new Document();

StructuredDocumentTag richText = new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(richText);

// 校验和是只读的，并使用相应的自定义 XML 数据部分的数据进行计算。
richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>ContentControl</text></root>"), "/root/text", "");

long checksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(checksum);

richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>Updated ContentControl</text></root>"), "/root/text", "");

long updatedChecksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(updatedChecksum);

// 我们更改了标记的 XmlPart，并且校验和在运行时更新。
Assert.AreNotEqual(checksum, updatedChecksum);
```

### 也可以看看

* class [CustomXmlPart](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
