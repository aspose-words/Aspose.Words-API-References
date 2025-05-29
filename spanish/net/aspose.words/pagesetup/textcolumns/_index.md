---
title: PageSetup.TextColumns
linktitle: TextColumns
articleTitle: TextColumns
second_title: Aspose.Words para .NET
description: Descubra la propiedad TextColumns de PageSetup, acceda a una colección versátil de columnas de texto para mejorar el diseño y el formato de su documento sin esfuerzo.
type: docs
weight: 420
url: /es/net/aspose.words/pagesetup/textcolumns/
---
## PageSetup.TextColumns property

Devuelve una colección que representa el conjunto de columnas de texto.

```csharp
public TextColumnCollection TextColumns { get; }
```

## Ejemplos

Muestra cómo crear múltiples columnas espaciadas uniformemente en una sección.

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

* class [TextColumnCollection](../../textcolumncollection/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
