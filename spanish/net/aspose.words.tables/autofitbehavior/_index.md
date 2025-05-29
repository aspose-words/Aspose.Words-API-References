---
title: AutoFitBehavior Enum
linktitle: AutoFitBehavior
articleTitle: AutoFitBehavior
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Tables.AutoFitBehavior para optimizar el cambio de tamaño de la tabla con el método AutoFit, mejorando el diseño y la presentación del documento.
type: docs
weight: 7080
url: /es/net/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enumeration

Determina cómo Aspose.Words redimensiona la tabla cuando invoca el[`AutoFit`](../table/autofit/) método.

```csharp
public enum AutoFitBehavior
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| AutoFitToContents | `0` | Aspose.Words habilita la opción Autoajuste, elimina el ancho preferido de la tabla y de todas las celdas y luego actualiza el diseño de la tabla. |
| AutoFitToWindow | `1` | Cuando utiliza este valor, Aspose.Words habilita la opción Autoajuste, establece el ancho preferido para la tabla al 100%, elimina los anchos preferidos de todas las celdas y luego actualiza el diseño de la tabla. |
| FixedColumnWidths | `2` | Aspose.Words deshabilita la opción Autoajuste y elimina el formato preferido de la tabla. |

## Ejemplos

Muestra cómo crear una nueva tabla mientras se aplica un estilo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

//Debemos insertar al menos una fila antes de establecer cualquier formato de tabla.
builder.InsertCell();

// Establezca el estilo de tabla utilizado en función del identificador de estilo.
// Tenga en cuenta que no todos los estilos de tabla están disponibles al guardar en formato .doc.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Aplicar parcialmente el estilo a las características de la tabla en función de los predicados y, luego, crear la tabla.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

Muestra cómo construir una tabla formateada de 2x2.

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

// Al construir la tabla, el generador de documentos aplicará sus valores de propiedad RowFormat/CellFormat actuales
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

// Las filas y celdas agregadas previamente no se ven afectadas retroactivamente por los cambios en el formato del generador.
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
