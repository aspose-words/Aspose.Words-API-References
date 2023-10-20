---
title: OleFormat.GetRawData
linktitle: GetRawData
articleTitle: GetRawData
second_title: Aspose.Words pour .NET
description: OleFormat GetRawData méthode. Obtient les données brutes de lobjet OLE en C#.
type: docs
weight: 150
url: /fr/net/aspose.words.drawing/oleformat/getrawdata/
---
## OleFormat.GetRawData method

Obtient les données brutes de l'objet OLE.

```csharp
public byte[] GetRawData()
```

## Exemples

Montre comment accéder aux données brutes d’un objet OLE incorporé.

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

### Voir également

* class [OleFormat](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
