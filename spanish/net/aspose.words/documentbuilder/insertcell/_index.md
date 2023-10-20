---
title: DocumentBuilder.InsertCell
linktitle: InsertCell
articleTitle: InsertCell
second_title: Aspose.Words para .NET
description: DocumentBuilder InsertCell método. Inserta una celda de tabla en el documento en C#.
type: docs
weight: 270
url: /es/net/aspose.words/documentbuilder/insertcell/
---
## DocumentBuilder.InsertCell method

Inserta una celda de tabla en el documento.

```csharp
public Cell InsertCell()
```

### Valor_devuelto

El nodo celular que se acaba de insertar.

## Observaciones

Para iniciar una mesa, simplemente llame`InsertCell` . Después de esto, cualquier contenido que agregue usando otros métodos del[`DocumentBuilder`](../) La clase se agregará a la celda actual.

Para iniciar una nueva celda en la misma fila, llame`InsertCell` de nuevo.

Para finalizar una llamada a una fila de la tabla[`EndRow`](../endrow/).

Utilizar el[`CellFormat`](../cellformat/)propiedad para especificar el formato de celda.

## Ejemplos

Muestra cómo utilizar un generador de documentos para crear una tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inicie la tabla, luego complete la primera fila con dos celdas.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Llame al método "EndRow" del constructor para iniciar una nueva fila.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

Muestra cómo crear una tabla con bordes personalizados.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Configurar opciones de formato de tabla para un creador de documentos
// los aplicará a cada fila y celda que agreguemos con ella.
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
// y cualquier celda nueva que creemos con el constructor posteriormente.
// Esto no afectará a las celdas que hayamos añadido anteriormente.
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

* class [Cell](../../../aspose.words.tables/cell/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
