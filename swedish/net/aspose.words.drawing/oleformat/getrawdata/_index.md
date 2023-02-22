---
title: OleFormat.GetRawData
second_title: Aspose.Words för .NET API Referens
description: OleFormat metod. Hämtar rådata för OLEobjekt.
type: docs
weight: 150
url: /sv/net/aspose.words.drawing/oleformat/getrawdata/
---
## OleFormat.GetRawData method

Hämtar rådata för OLE-objekt.

```csharp
public byte[] GetRawData()
```

### Exempel

Visar hur man kommer åt rådata för ett inbäddat OLE-objekt.

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

### Se även

* class [OleFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../oleformat/)
* hopsättning [Aspose.Words](../../../)


