---
title: OleFormat.GetRawData
linktitle: GetRawData
articleTitle: GetRawData
second_title: Aspose.Words per .NET
description: Scopri il metodo GetRawData di OleFormat per recuperare facilmente i dati grezzi degli oggetti OLE, migliorando le tue capacità di gestione e integrazione dei dati.
type: docs
weight: 150
url: /it/net/aspose.words.drawing/oleformat/getrawdata/
---
## OleFormat.GetRawData method

Ottiene i dati grezzi dell'oggetto OLE.

```csharp
public byte[] GetRawData()
```

## Esempi

Mostra come accedere ai dati grezzi di un oggetto OLE incorporato.

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

### Guarda anche

* class [OleFormat](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
