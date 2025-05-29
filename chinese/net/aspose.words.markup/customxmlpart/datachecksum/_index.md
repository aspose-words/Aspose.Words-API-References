---
title: CustomXmlPart.DataChecksum
linktitle: DataChecksum
articleTitle: DataChecksum
second_title: Aspose.Words for .NET
description: 探索 CustomXmlPart DataChecksum 属性，使用可靠的 CRC 校验和来确保 XML 内容的数据完整性。提升数据的可靠性！
type: docs
weight: 30
url: /zh/net/aspose.words.markup/customxmlpart/datachecksum/
---
## CustomXmlPart.DataChecksum property

指定循环冗余校验 (CRC)[`Data`](../data/)内容.

```csharp
public long DataChecksum { get; }
```

## 例子

显示在运行时如何计算校验和。

```csharp
Document doc = new Document();

StructuredDocumentTag richText = new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(richText);

// 校验和是只读的，使用相应的自定义 XML 数据部分的数据计算。
richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>ContentControl</text></root>"), "/root/text", "");

long checksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(checksum);

richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>Updated ContentControl</text></root>"), "/root/text", "");

long updatedChecksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(updatedChecksum);

// 我们改变了标签的 XmlPart，并且校验和在运行时更新。
Assert.AreNotEqual(checksum, updatedChecksum);
```

### 也可以看看

* class [CustomXmlPart](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
