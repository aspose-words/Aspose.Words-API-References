---
title: Table.TextWrapping
linktitle: TextWrapping
articleTitle: TextWrapping
second_title: Aspose.Words para .NET
description: Descubre la propiedad Table TextWrapping para gestionar fácilmente el flujo de texto en tus tablas. ¡Mejora la legibilidad y el diseño con opciones de texto flexibles!
type: docs
weight: 310
url: /es/net/aspose.words.tables/table/textwrapping/
---
## Table.TextWrapping property

Obtiene o establece`TextWrapping` para la tabla.

```csharp
public TextWrapping TextWrapping { get; set; }
```

## Ejemplos

Muestra cómo trabajar con el ajuste de texto de una tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

builder.Font.Size = 16;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Establezca la propiedad "TextWrapping" en "TextWrapping.Around" para que la tabla ajuste el texto a su alrededor.
// y empújelo hacia abajo en el párrafo siguiente estableciendo la posición.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### Ver también

* enum [TextWrapping](../../textwrapping/)
* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
