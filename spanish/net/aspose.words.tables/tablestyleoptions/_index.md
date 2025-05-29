---
title: TableStyleOptions Enum
linktitle: TableStyleOptions
articleTitle: TableStyleOptions
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Tables.TableStyleOptions para crear estilos de tabla flexibles. ¡Mejore el diseño de sus documentos con estilos de tabla personalizables hoy mismo!
type: docs
weight: 7220
url: /es/net/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enumeration

Especifica cómo se aplica el estilo de tabla a una tabla.

```csharp
[Flags]
public enum TableStyleOptions
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | No se aplica ningún formato de estilo de tabla. |
| FirstRow | `20` | Aplicar formato condicional de la primera fila. |
| LastRow | `40` | Aplicar formato condicional de última fila. |
| FirstColumn | `80` | Aplicar formato condicional a la primera columna. |
| LastColumn | `100` | Aplicar formato condicional a la última columna. |
| RowBands | `200` | Aplicar formato condicional de bandas de filas. |
| ColumnBands | `400` | Aplicar formato condicional de bandas de columnas. |
| Default2003 | `600` | Se aplican bandas de filas y columnas. Esta es la configuración predeterminada de Microsoft Word para formatos antiguos como DOC, WML y RTF. |
| Default | `2A0` | Estos son los valores predeterminados de Microsoft Word. |

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

* property [StyleOptions](../table/styleoptions/)
* espacio de nombres [Aspose.Words.Tables](../../aspose.words.tables/)
* asamblea [Aspose.Words](../../)
