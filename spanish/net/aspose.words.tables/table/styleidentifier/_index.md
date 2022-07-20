---
title: StyleIdentifier
second_title: Referencia de API de Aspose.Words para .NET
description: Obtiene o establece el identificador de estilo independiente de la configuración regional del estilo de tabla aplicado a esta tabla.
type: docs
weight: 280
url: /es/net/aspose.words.tables/table/styleidentifier/
---
## Table.StyleIdentifier property

Obtiene o establece el identificador de estilo independiente de la configuración regional del estilo de tabla aplicado a esta tabla.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

### Ejemplos

Muestra cómo construir una nueva tabla mientras se aplica un estilo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Debemos insertar al menos una fila antes de configurar cualquier formato de tabla.
builder.InsertCell();

// Establezca el estilo de tabla utilizado en función del identificador de estilo.
// Tenga en cuenta que no todos los estilos de tabla están disponibles al guardar en formato .doc.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Aplique parcialmente el estilo a las características de la tabla en función de los predicados, luego construya la tabla.
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

* enum [StyleIdentifier](../../../aspose.words/styleidentifier)
* class [Table](../../table)
* espacio de nombres [Aspose.Words.Tables](../../table)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->