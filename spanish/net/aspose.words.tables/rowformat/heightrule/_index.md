---
title: RowFormat.HeightRule
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words para .NET
description: RowFormat HeightRule propiedad. Obtiene o establece la regla para determinar la altura de la fila de la tabla en C#.
type: docs
weight: 50
url: /es/net/aspose.words.tables/rowformat/heightrule/
---
## RowFormat.HeightRule property

Obtiene o establece la regla para determinar la altura de la fila de la tabla.

```csharp
public HeightRule HeightRule { get; set; }
```

## Ejemplos

Muestra cómo dar formato a filas con un generador de documentos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Inicie una segunda fila y luego configure su altura. El constructor aplicará esta configuración a
// su fila actual, así como cualquier fila nueva que cree posteriormente.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// La primera fila no se vio afectada por la reconfiguración del relleno y aún mantiene los valores predeterminados.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

Muestra cómo crear una tabla formateada usando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
table.LeftIndent = 20;

// Establece algunas opciones de formato para el texto y la apariencia de la tabla.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// Configurar las opciones de formato en un generador de documentos las aplicará
// a la celda/fila actual en la que se encuentra el cursor,
// así como cualquier celda y fila nueva creada con ese generador.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// Reconfigurar los objetos de formato del constructor para las nuevas filas y celdas que estamos a punto de crear.
// El constructor no los aplicará a la primera fila ya creada para que se destaque como fila de encabezado.
builder.CellFormat.Shading.BackgroundPatternColor = Color.White;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.RowFormat.Height = 30;
builder.RowFormat.HeightRule = HeightRule.Auto;
builder.InsertCell();
builder.Font.Size = 12;
builder.Font.Bold = false;

builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");
builder.InsertCell();
builder.Write("Row 1, Cell 3.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.InsertCell();
builder.Write("Row 2, Cell 3.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateFormattedTable.docx");
```

### Ver también

* enum [HeightRule](../../../aspose.words/heightrule/)
* class [RowFormat](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
