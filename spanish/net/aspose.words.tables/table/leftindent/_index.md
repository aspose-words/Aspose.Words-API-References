---
title: Table.LeftIndent
second_title: Referencia de API de Aspose.Words para .NET
description: Table propiedad. Obtiene o establece el valor que representa la sangría izquierda de la tabla.
type: docs
weight: 190
url: /es/net/aspose.words.tables/table/leftindent/
---
## Table.LeftIndent property

Obtiene o establece el valor que representa la sangría izquierda de la tabla.

```csharp
public double LeftIndent { get; set; }
```

### Ejemplos

Muestra cómo crear una tabla con formato utilizando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
table.LeftIndent = 20;

// Establecer algunas opciones de formato para el texto y la apariencia de la tabla.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// La configuración de las opciones de formato en un generador de documentos las aplicará
// a la celda/fila actual en la que se encuentra el cursor,
// así como las nuevas celdas y filas creadas con ese constructor.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// Reconfigure los objetos de formato del constructor para nuevas filas y celdas que estamos a punto de crear.
// El constructor no los aplicará a la primera fila ya creada para que se destaque como una fila de encabezado.
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

* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../table/)
* asamblea [Aspose.Words](../../../)


