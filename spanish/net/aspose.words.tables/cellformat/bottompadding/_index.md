---
title: CellFormat.BottomPadding
linktitle: BottomPadding
articleTitle: BottomPadding
second_title: Aspose.Words para .NET
description: Descubra la propiedad CellFormat BottomPadding para personalizar el espaciado de sus celdas. Mejore sus diseños con ajustes precisos de puntos para una mejor presentación.
type: docs
weight: 20
url: /es/net/aspose.words.tables/cellformat/bottompadding/
---
## CellFormat.BottomPadding property

Devuelve o establece la cantidad de espacio (en puntos) que se agregará debajo del contenido de la celda.

```csharp
public double BottomPadding { get; set; }
```

## Ejemplos

Muestra cómo formatear celdas con un generador de documentos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Inserte una segunda celda y luego configure las opciones de relleno de texto de la celda.
// El constructor aplicará estas configuraciones en su celda actual y en cualquier celda nueva que cree posteriormente.
builder.InsertCell();

CellFormat cellFormat = builder.CellFormat;
cellFormat.Width = 250;
cellFormat.LeftPadding = 30;
cellFormat.RightPadding = 30;
cellFormat.TopPadding = 30;
cellFormat.BottomPadding = 30;

builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.EndTable();

// La primera celda no se vio afectada por la reconfiguración del relleno y aún conserva los valores predeterminados.
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.Width);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.LeftPadding);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.RightPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.TopPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.BottomPadding);

Assert.AreEqual(250.0d, table.FirstRow.Cells[1].CellFormat.Width);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.LeftPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.RightPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.TopPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.BottomPadding);

// La primera celda seguirá creciendo en el documento de salida para coincidir con el tamaño de la celda vecina.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

### Ver también

* class [CellFormat](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
