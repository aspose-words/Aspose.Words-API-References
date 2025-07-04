---
title: OleFormat.GetRawData
linktitle: GetRawData
articleTitle: GetRawData
second_title: Aspose.Words for .NET
description: Discover OleFormat's GetRawData method to easily retrieve OLE object raw data, enhancing your data management and integration capabilities.
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

        Assert.That(oleRawData.Length, Is.EqualTo(24576));
    }
}
```

### See Also

* class [OleFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
