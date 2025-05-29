---
title: Table.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words para .NET
description: Descubra la propiedad Table StyleIdentifier para administrar fácilmente estilos de tabla independientes de la configuración regional, mejorando la presentación de sus datos sin esfuerzo.
type: docs
weight: 280
url: /es/net/aspose.words.tables/table/styleidentifier/
---
## Table.StyleIdentifier property

Obtiene o establece el identificador de estilo independiente de la configuración regional del estilo de tabla aplicado a esta tabla.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

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

### Ver también

* enum [StyleIdentifier](../../../aspose.words/styleidentifier/)
* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
