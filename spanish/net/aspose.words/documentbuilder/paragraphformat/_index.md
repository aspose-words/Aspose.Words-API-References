---
title: DocumentBuilder.ParagraphFormat
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBuilder propiedad. Devuelve un objeto que representa las propiedades de formato del párrafo actual.
type: docs
weight: 170
url: /es/net/aspose.words/documentbuilder/paragraphformat/
---
## DocumentBuilder.ParagraphFormat property

Devuelve un objeto que representa las propiedades de formato del párrafo actual.

```csharp
public ParagraphFormat ParagraphFormat { get; }
```

### Ejemplos

Muestra cómo crear una tabla formateada usando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
table.LeftIndent = 20;

// Establece algunas opciones de formato para el texto y la apariencia de la tabla.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// Configurar las opciones de formato en un generador de documentos las aplicará
// a la celda/fila actual en la que se encuentra el cursor,
// así como cualquier celda y fila nueva creada con ese generador.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// Reconfigurar los objetos de formato del constructor para las nuevas filas y celdas que estamos a punto de crear.
// El constructor no los aplicará a la primera fila ya creada para que se destaque como fila de encabezado.
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

* class [ParagraphFormat](../../paragraphformat/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)


