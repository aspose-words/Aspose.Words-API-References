---
title: Enum TableStyleOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Tables.TableStyleOptions enumeración. Especifica cómo se aplica el estilo de tabla a una tabla.
type: docs
weight: 6370
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
| FirstRow | `20` | Aplicar formato condicional a la primera fila. |
| LastRow | `40` | Aplicar formato condicional a la última fila. |
| FirstColumn | `80` | Aplicar formato condicional a la primera columna. |
| LastColumn | `100` | Aplicar formato condicional a la última columna. |
| RowBands | `200` | Aplicar formato condicional de bandas de filas. |
| ColumnBands | `400` | Aplicar formato condicional de bandas de columnas. |
| Default2003 | `600` | Se aplican bandas de filas y columnas. Este es el valor predeterminado de Microsoft Word para formatos antiguos como DOC, WML y RTF. |
| Default | `2A0` | Este es el valor predeterminado de Microsoft Word. |

### Ejemplos

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

* property [StyleOptions](../table/styleoptions/)
* espacio de nombres [Aspose.Words.Tables](../../aspose.words.tables/)
* asamblea [Aspose.Words](../../)


