---
title: Row.RowFormat
linktitle: RowFormat
articleTitle: RowFormat
second_title: Aspose.Words para .NET
description: Descubra la propiedad Row RowFormat para acceder fácilmente a opciones de formato de fila personalizables, mejorando la presentación de sus datos sin esfuerzo.
type: docs
weight: 110
url: /es/net/aspose.words.tables/row/rowformat/
---
## Row.RowFormat property

Proporciona acceso a las propiedades de formato de la fila.

```csharp
public RowFormat RowFormat { get; }
```

## Ejemplos

Muestra cómo modificar el formato de una fila de una tabla.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Utilice la propiedad "RowFormat" de la primera fila para establecer el formato que modifica la apariencia de toda esa fila.
Row firstRow = table.FirstRow;
firstRow.RowFormat.Borders.LineStyle = LineStyle.None;
firstRow.RowFormat.HeightRule = HeightRule.Auto;
firstRow.RowFormat.AllowBreakAcrossPages = true;

doc.Save(ArtifactsDir + "Table.RowFormat.docx");
```

Muestra cómo modificar el formato de filas y celdas en una tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("City");
builder.InsertCell();
builder.Write("Country");
builder.EndRow();
builder.InsertCell();
builder.Write("London");
builder.InsertCell();
builder.Write("U.K.");
builder.EndTable();

// Utilice la propiedad "RowFormat" de la primera fila para modificar el formato
// del contenido de todas las celdas de esta fila.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Utilice la propiedad "CellFormat" de la primera celda de la última fila para modificar el formato del contenido de esa celda.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

### Ver también

* class [RowFormat](../../rowformat/)
* class [Row](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
