---
title: TextOrientation Enum
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words para .NET
description: Aspose.Words.TextOrientation enumeración. Especifica la orientación del texto en una página en una celda de una tabla o en un marco de texto en C#.
type: docs
weight: 6430
url: /es/net/aspose.words/textorientation/
---
## TextOrientation enumeration

Especifica la orientación del texto en una página, en una celda de una tabla o en un marco de texto.

```csharp
public enum TextOrientation
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Horizontal | `0` | El texto está organizado horizontalmente (lr-tb). |
| Downward | `1` | El texto se gira 90 grados hacia la derecha para aparecer de arriba a abajo (tb-rl). |
| Upward | `3` | El texto se gira 90 grados hacia la izquierda para aparecer de abajo hacia arriba (bt-lr). |
| HorizontalRotatedFarEast | `4` | El texto está organizado horizontalmente, pero los caracteres del Lejano Oriente están girados 90 grados hacia la izquierda (lr-tb-v). |
| VerticalFarEast | `5` | Los caracteres del Lejano Oriente aparecen verticales, el resto del texto se gira 90 grados hacia la derecha para aparecer de arriba a abajo (tb-rl-v). |
| VerticalRotatedFarEast | `7` | Los caracteres del Lejano Oriente aparecen verticales, el resto del texto se gira 90 grados hacia la derecha para aparecer de arriba a abajo verticalmente, luego de izquierda a derecha horizontalmente (tb-lr-v). |

## Ejemplos

Muestra cómo crear una tabla formateada de 2x2.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// Mientras crea la tabla, el creador de documentos aplicará sus valores actuales de propiedad RowFormat/CellFormat
// a la fila/celda actual en la que se encuentra el cursor y a cualquier fila/celda nueva a medida que las crea.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Las filas y celdas agregadas anteriormente no se ven afectadas retroactivamente por los cambios en el formato del constructor.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
