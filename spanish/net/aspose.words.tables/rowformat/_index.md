---
title: RowFormat Class
linktitle: RowFormat
articleTitle: RowFormat
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Tables.RowFormat para un formato completo de filas de tablas. Mejore el diseño de sus documentos con funciones potentes y flexibles.
type: docs
weight: 7180
url: /es/net/aspose.words.tables/rowformat/
---
## RowFormat class

Representa todo el formato de una fila de la tabla.

Para obtener más información, visite el[Trabajar con tablas](https://docs.aspose.com/words/net/working-with-tables/) Artículo de documentación.

```csharp
public class RowFormat
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AllowBreakAcrossPages](../../aspose.words.tables/rowformat/allowbreakacrosspages/) { get; set; } | Verdadero si se permite que el texto de una fila de tabla se divida en un salto de página. |
| [Borders](../../aspose.words.tables/rowformat/borders/) { get; } | Obtiene la colección de bordes de celda predeterminados para la fila. |
| [HeadingFormat](../../aspose.words.tables/rowformat/headingformat/) { get; set; } | Verdadero si la fila se repite como encabezado de tabla en cada página cuando la tabla abarca más de una página. |
| [Height](../../aspose.words.tables/rowformat/height/) { get; set; } | Obtiene o establece la altura de la fila de la tabla en puntos. |
| [HeightRule](../../aspose.words.tables/rowformat/heightrule/) { get; set; } | Obtiene o establece la regla para determinar la altura de la fila de la tabla. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/rowformat/clearformatting/)() | Restablece el formato de fila predeterminado. |

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

Muestra cómo crear una tabla con bordes personalizados.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Configuración de opciones de formato de tabla para un generador de documentos
// los aplicará a cada fila y celda que agreguemos.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

//Cambiar el formato se aplicará a la celda actual,
// y cualquier celda nueva que creemos con el constructor posteriormente.
//Esto no afectará las celdas que hemos agregado previamente.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Aumenta la altura de la fila para que se ajuste al texto vertical.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Tables](../../aspose.words.tables/)
* asamblea [Aspose.Words](../../)
