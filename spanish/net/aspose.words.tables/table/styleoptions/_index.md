---
title: Table.StyleOptions
linktitle: StyleOptions
articleTitle: StyleOptions
second_title: Aspose.Words para .NET
description: Table StyleOptions propiedad. Obtiene o establece indicadores de bits que especifican cómo se aplica un estilo de tabla a esta tabla en C#.
type: docs
weight: 300
url: /es/net/aspose.words.tables/table/styleoptions/
---
## Table.StyleOptions property

Obtiene o establece indicadores de bits que especifican cómo se aplica un estilo de tabla a esta tabla.

```csharp
public TableStyleOptions StyleOptions { get; set; }
```

## Ejemplos

Muestra cómo crear una nueva tabla mientras se aplica un estilo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Debemos insertar al menos una fila antes de configurar cualquier formato de tabla.
builder.InsertCell();

// Establece el estilo de tabla utilizado según el identificador de estilo.
// Tenga en cuenta que no todos los estilos de tabla están disponibles al guardar en formato .doc.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Aplique parcialmente el estilo a las características de la tabla según los predicados y luego cree la tabla.
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

* enum [TableStyleOptions](../../tablestyleoptions/)
* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
