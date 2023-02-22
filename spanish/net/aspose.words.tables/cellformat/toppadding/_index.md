---
title: CellFormat.TopPadding
second_title: Referencia de API de Aspose.Words para .NET
description: CellFormat propiedad. Devuelve o establece la cantidad de espacio en puntos para agregar encima del contenido de la celda.
type: docs
weight: 100
url: /es/net/aspose.words.tables/cellformat/toppadding/
---
## CellFormat.TopPadding property

Devuelve o establece la cantidad de espacio (en puntos) para agregar encima del contenido de la celda.

```csharp
public double TopPadding { get; set; }
```

### Ejemplos

Muestra cómo formatear celdas con un generador de documentos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Inserte una segunda celda y luego configure las opciones de relleno del texto de la celda.
// El constructor aplicará esta configuración en su celda actual, y cualquier celda nueva se creará después.
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

// La primera celda aún crecerá en el documento de salida para coincidir con el tamaño de su celda vecina.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

### Ver también

* class [CellFormat](../)
* espacio de nombres [Aspose.Words.Tables](../../cellformat/)
* asamblea [Aspose.Words](../../../)


