---
title: DocumentBuilder.Font
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBuilder propiedad. Devuelve un objeto que representa las propiedades de formato de fuente actuales.
type: docs
weight: 100
url: /es/net/aspose.words/documentbuilder/font/
---
## DocumentBuilder.Font property

Devuelve un objeto que representa las propiedades de formato de fuente actuales.

```csharp
public Font Font { get; }
```

### Observaciones

Usar`Font` para acceder y modificar las propiedades de formato de fuente.

Especifique el formato de fuente antes de insertar texto.

### Ejemplos

Muestra cómo insertar una cadena rodeada por un borde en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

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

* class [Font](../../font/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)


