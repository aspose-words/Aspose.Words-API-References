---
title: GetRawData
second_title: Aspose.Words für .NET-API-Referenz
description: Ruft Rohdaten des OLE-Objekts ab.
type: docs
weight: 150
url: /de/net/aspose.words.drawing/oleformat/getrawdata/
---
## OleFormat.GetRawData method

Ruft Rohdaten des OLE-Objekts ab.

```csharp
public byte[] GetRawData()
```

### Beispiele

Zeigt, wie auf die Rohdaten eines eingebetteten OLE-Objekts zugegriffen wird.

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

### Siehe auch

* class [OleFormat](../../oleformat)
* namensraum [Aspose.Words.Drawing](../../oleformat)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
