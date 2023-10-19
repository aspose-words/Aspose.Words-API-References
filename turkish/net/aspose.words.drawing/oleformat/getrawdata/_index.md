---
title: OleFormat.GetRawData
linktitle: GetRawData
articleTitle: GetRawData
second_title: Aspose.Words for .NET
description: OleFormat GetRawData yöntem. OLE nesnesinin ham verilerini alır C#'da.
type: docs
weight: 150
url: /tr/net/aspose.words.drawing/oleformat/getrawdata/
---
## OleFormat.GetRawData method

OLE nesnesinin ham verilerini alır.

```csharp
public byte[] GetRawData()
```

## Örnekler

Katıştırılmış bir OLE nesnesinin ham verilerine nasıl erişileceğini gösterir.

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

### Ayrıca bakınız

* class [OleFormat](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
