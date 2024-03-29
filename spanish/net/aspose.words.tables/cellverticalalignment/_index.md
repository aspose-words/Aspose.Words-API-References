---
title: CellVerticalAlignment Enum
linktitle: CellVerticalAlignment
articleTitle: CellVerticalAlignment
second_title: Aspose.Words para .NET
description: Aspose.Words.Tables.CellVerticalAlignment enumeración. Especifica la justificación vertical del texto dentro de una celda de la tabla en C#.
type: docs
weight: 6280
url: /es/net/aspose.words.tables/cellverticalalignment/
---
## CellVerticalAlignment enumeration

Especifica la justificación vertical del texto dentro de una celda de la tabla.

```csharp
public enum CellVerticalAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Top | `0` | El texto está alineado en la parte superior de una celda. |
| Center | `1` | El texto está alineado en el medio de una celda. |
| Bottom | `2` | El texto está alineado en la parte inferior de la celda. |

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

* espacio de nombres [Aspose.Words.Tables](../../aspose.words.tables/)
* asamblea [Aspose.Words](../../)
