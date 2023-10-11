---
title: Enum TextWrapping
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Tables.TextWrapping enumeración. Especifica cómo se ajusta el texto alrededor de la tabla.
type: docs
weight: 6380
url: /es/net/aspose.words.tables/textwrapping/
---
## TextWrapping enumeration

Especifica cómo se ajusta el texto alrededor de la tabla.

```csharp
public enum TextWrapping
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | El texto y la tabla se muestran en el orden en que aparecen en el documento. |
| Around | `1` | El texto se ajusta alrededor de la tabla ocupando el espacio lateral disponible. |
| Default | `0` | Valor predeterminado. |

### Ejemplos

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

// Establece la propiedad "TextWrapping" en "TextWrapping.Around" para que la tabla ajuste el texto a su alrededor,
// y empújelo hacia abajo en el párrafo siguiente estableciendo la posición.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Tables](../../aspose.words.tables/)
* asamblea [Aspose.Words](../../)


