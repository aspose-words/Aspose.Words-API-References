---
title: OleFormat.GetRawData
linktitle: GetRawData
articleTitle: GetRawData
second_title: 用于 .NET 的 Aspose.Words
description: OleFormat GetRawData 方法. 获取 OLE 对象原始数据 在 C#.
type: docs
weight: 150
url: /zh/net/aspose.words.drawing/oleformat/getrawdata/
---
## OleFormat.GetRawData method

获取 OLE 对象原始数据。

```csharp
public byte[] GetRawData()
```

## 例子

演示如何访问嵌入式 OLE 对象的原始数据。

```csharp
Document doc = new Document(MyDir + "OLE objects.docx");

foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true))
{
    OleFormat oleFormat = shape.OleFormat;
    if (oleFormat != null)
    {
        Console.WriteLine($"This is {(oleFormat.IsLink ? "a linked" : "an embedded")} object");
        byte[] oleRawData = oleFormat.GetRawData();

        Assert.AreEqual(24576, oleRawData.Length);
    }
}
```

### 也可以看看

* class [OleFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
