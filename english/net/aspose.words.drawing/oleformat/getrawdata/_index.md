---
title: OleFormat.GetRawData
linktitle: GetRawData
articleTitle: GetRawData
second_title: Aspose.Words for .NET
description: OleFormat GetRawData method. Gets OLE object raw data in C#.
type: docs
weight: 150
url: /net/aspose.words.drawing/oleformat/getrawdata/
---
## OleFormat.GetRawData method

Gets OLE object raw data.

```csharp
public byte[] GetRawData()
```

## Examples

Shows how to access the raw data of an embedded OLE object.

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

### See Also

* class [OleFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
