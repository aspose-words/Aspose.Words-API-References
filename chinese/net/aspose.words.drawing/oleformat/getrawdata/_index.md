---
title: OleFormat.GetRawData
linktitle: GetRawData
articleTitle: GetRawData
second_title: Aspose.Words for .NET
description: 探索 OleFormat 的 GetRawData 方法，轻松检索 OLE 对象原始数据，增强您的数据管理和集成能力。
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

展示如何访问嵌入的 OLE 对象的原始数据。

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
