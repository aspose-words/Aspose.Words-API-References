---
title: RowFormat.HeadingFormat
second_title: Referencia de API de Aspose.Words para .NET
description: RowFormat propiedad. Verdadero si la fila se repite como encabezado de tabla en cada página cuando la tabla abarca más de una página.
type: docs
weight: 30
url: /es/net/aspose.words.tables/rowformat/headingformat/
---
## RowFormat.HeadingFormat property

Verdadero si la fila se repite como encabezado de tabla en cada página cuando la tabla abarca más de una página.

```csharp
public bool HeadingFormat { get; set; }
```

### Ejemplos

Muestra cómo construir una tabla con filas que se repiten en cada página.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// Cualquier fila insertada mientras el indicador "HeadingFormat" está establecido en "true"
// aparecerá en la parte superior de la tabla en cada página que abarque.
builder.RowFormat.HeadingFormat = true;
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.CellFormat.Width = 100;
builder.InsertCell();
builder.Write("Heading row 1");
builder.EndRow();
builder.InsertCell();
builder.Write("Heading row 2");
builder.EndRow();

builder.CellFormat.Width = 50;
builder.ParagraphFormat.ClearFormatting();
builder.RowFormat.HeadingFormat = false;

// Agregue suficientes filas para que la tabla abarque dos páginas.
for (int i = 0; i < 50; i++)
{
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 1.");
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 2.");
    builder.EndRow();
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableSetHeadingRow.docx");
```

### Ver también

* class [RowFormat](../)
* espacio de nombres [Aspose.Words.Tables](../../rowformat/)
* asamblea [Aspose.Words](../../../)


