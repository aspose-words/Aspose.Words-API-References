---
title: TextColumnCollection.SetCount
linktitle: SetCount
articleTitle: SetCount
second_title: Aspose.Words para .NET
description: TextColumnCollection SetCount método. Organiza el texto en el número especificado de columnas de texto en C#.
type: docs
weight: 70
url: /es/net/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection.SetCount method

Organiza el texto en el número especificado de columnas de texto.

```csharp
public void SetCount(int newCount)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| newCount | Int32 | El número de columnas en las que se organizará el texto. |

## Observaciones

Cuando[`EvenlySpaced`](../evenlyspaced/) es`FALSO` y aumentas el numero de columnas, new[`TextColumn`](../../textcolumn/) los objetos se crean con ancho y espaciado cero. Debe establecer el ancho y el espaciado para las nuevas columnas.

## Ejemplos

Muestra cómo crear varias columnas espaciadas uniformemente en una sección.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### Ver también

* class [TextColumnCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
