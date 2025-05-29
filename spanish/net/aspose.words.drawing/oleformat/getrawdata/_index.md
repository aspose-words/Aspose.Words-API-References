---
title: OleFormat.GetRawData
linktitle: GetRawData
articleTitle: GetRawData
second_title: Aspose.Words para .NET
description: Descubra el método GetRawData de OleFormat para recuperar fácilmente datos sin procesar de objetos OLE, mejorando sus capacidades de integración y gestión de datos.
type: docs
weight: 150
url: /es/net/aspose.words.drawing/oleformat/getrawdata/
---
## OleFormat.GetRawData method

Obtiene datos sin procesar del objeto OLE.

```csharp
public byte[] GetRawData()
```

## Ejemplos

Muestra cómo acceder a los datos sin procesar de un objeto OLE incrustado.

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

### Ver también

* class [OleFormat](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
