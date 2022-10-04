---
title: CellFormat
second_title: Referencia de API de Aspose.Words para .NET
description: Representa todo el formato de una celda de tabla.
type: docs
weight: 5960
url: /es/net/aspose.words.tables/cellformat/
---
## CellFormat class

Representa todo el formato de una celda de tabla.

```csharp
public class CellFormat
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Borders](../../aspose.words.tables/cellformat/borders/) { get; } | Obtiene la colección de bordes de la celda. |
| [BottomPadding](../../aspose.words.tables/cellformat/bottompadding/) { get; set; } | Devuelve o establece la cantidad de espacio (en puntos) para agregar debajo del contenido de la celda. |
| [FitText](../../aspose.words.tables/cellformat/fittext/) { get; set; } | Si es verdadero, ajusta el texto en la celda, comprimiendo cada párrafo al ancho de la celda. |
| [HorizontalMerge](../../aspose.words.tables/cellformat/horizontalmerge/) { get; set; } | Especifica cómo se fusiona la celda horizontalmente con otras celdas de la fila. |
| [LeftPadding](../../aspose.words.tables/cellformat/leftpadding/) { get; set; } | Devuelve o establece la cantidad de espacio (en puntos) a agregar a la izquierda del contenido de la celda. |
| [Orientation](../../aspose.words.tables/cellformat/orientation/) { get; set; } | Devuelve o establece la orientación del texto en una celda de tabla. |
| [PreferredWidth](../../aspose.words.tables/cellformat/preferredwidth/) { get; set; } | Devuelve o establece el ancho preferido de la celda. |
| [RightPadding](../../aspose.words.tables/cellformat/rightpadding/) { get; set; } | Devuelve o establece la cantidad de espacio (en puntos) a agregar a la derecha del contenido de la celda. |
| [Shading](../../aspose.words.tables/cellformat/shading/) { get; } | Devuelve un objeto Shading que hace referencia al formato de sombreado de la celda. |
| [TopPadding](../../aspose.words.tables/cellformat/toppadding/) { get; set; } | Devuelve o establece la cantidad de espacio (en puntos) para agregar encima del contenido de la celda. |
| [VerticalAlignment](../../aspose.words.tables/cellformat/verticalalignment/) { get; set; } | Devuelve o establece la alineación vertical del texto en la celda. |
| [VerticalMerge](../../aspose.words.tables/cellformat/verticalmerge/) { get; set; } | Especifica cómo se fusiona la celda con otras celdas verticalmente. |
| [Width](../../aspose.words.tables/cellformat/width/) { get; set; } | Obtiene el ancho de la celda en puntos. |
| [WrapText](../../aspose.words.tables/cellformat/wraptext/) { get; set; } | Si es verdadero, ajusta el texto de la celda. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/cellformat/clearformatting/)() | Restablece el formato de celda predeterminado. No cambia el ancho de la celda. |
| [SetPaddings](../../aspose.words.tables/cellformat/setpaddings/)(double, double, double, double) | Establece la cantidad de espacio (en puntos) para agregar a la izquierda/arriba/derecha/abajo del contenido de la celda. |

### Ejemplos

Muestra cómo modificar el formato de una celda de tabla.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// Use la propiedad "CellFormat" de una celda para establecer un formato que modifique la apariencia de esa celda.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
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

// Usa la propiedad "RowFormat" de la primera fila para modificar el formato
// del contenido de todas las celdas de esta fila.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Use la propiedad "CellFormat" de la primera celda en la última fila para modificar el formato del contenido de esa celda.
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

// Establecer opciones de formato de tabla para un generador de documentos
// los aplicará a cada fila y celda que agreguemos con él.
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

// Cambiar el formato lo aplicará a la celda actual,
// y cualquier celda nueva que creemos con el constructor después.
// Esto no afectará a las celdas que hemos agregado previamente.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
