---
title: Shading.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words para .NET
description: Elimina fácilmente el sombreado de tus objetos con nuestro método ClearFormatting. ¡Mejora tus diseños para un aspecto profesional y pulido!
type: docs
weight: 80
url: /es/net/aspose.words/shading/clearformatting/
---
## Shading.ClearFormatting method

Elimina el sombreado del objeto.

```csharp
public void ClearFormatting()
```

## Ejemplos

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

* class [Shading](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
