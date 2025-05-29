---
title: CellFormat.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words para .NET
description: Descubra la propiedad Ancho de CellFormat para medir fácilmente el ancho de celda en puntos, mejorando el diseño y la legibilidad de su hoja de cálculo.
type: docs
weight: 140
url: /es/net/aspose.words.tables/cellformat/width/
---
## CellFormat.Width property

Obtiene el ancho de la celda en puntos.

```csharp
public double Width { get; set; }
```

## Observaciones

El ancho lo calcula Aspose.Words al cargar y guardar el documento. Actualmente, no se admiten todas las combinaciones de propiedades de tabla, celda y documento. El valor devuelto puede no ser preciso para algunos documentos. Puede no coincidir exactamente con el ancho de celda calculado por MS Word cuando el documento se abre en MS Word.

No se recomienda configurar esta propiedad. No hay garantía de que la celda realmente tenga el ancho establecido. El ancho se puede ajustar para acomodar el contenido de la celda en un diseño de tabla de ajuste automático. Las celdas en otras filas pueden tener configuraciones de ancho conflictivas. La tabla se puede redimensionar para que encaje en el contenedor o para cumplir con las configuraciones de ancho de la tabla. Considere usar[`PreferredWidth`](../preferredwidth/)para establecer el ancho de celda. Al establecer esta propiedad se establecen[`PreferredWidth`](../preferredwidth/) implícitamente desde la versión 15.8.

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

* class [CellFormat](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
