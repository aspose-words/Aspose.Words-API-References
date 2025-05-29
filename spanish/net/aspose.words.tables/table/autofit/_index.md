---
title: Table.AutoFit
linktitle: AutoFit
articleTitle: AutoFit
second_title: Aspose.Words para .NET
description: Descubre el método Autoajuste de Tablas para redimensionar tablas y celdas fácilmente y optimizar el diseño. ¡Mejora la presentación de tus documentos fácilmente!
type: docs
weight: 380
url: /es/net/aspose.words.tables/table/autofit/
---
## Table.AutoFit method

Redimensiona la tabla y las celdas según el comportamiento de ajuste automático especificado.

```csharp
public void AutoFit(AutoFitBehavior behavior)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| behavior | AutoFitBehavior | Especifica cómo ajustar automáticamente la tabla. |

## Observaciones

Este método imita los comandos disponibles en el menú Autoajuste de una tabla en Microsoft Word. Los comandos disponibles son "Autoajustar al contenido", "Autoajustar a la ventana" y "Ancho de columna fijo". En Microsoft Word, estos comandos establecen las propiedades relevantes de la tabla y luego actualizan el diseño de la tabla, y Aspose.Words hace lo mismo.

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

* enum [AutoFitBehavior](../../autofitbehavior/)
* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
