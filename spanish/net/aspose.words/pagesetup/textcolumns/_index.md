---
title: PageSetup.TextColumns
second_title: Referencia de API de Aspose.Words para .NET
description: PageSetup propiedad. Devuelve una colección que representa el conjunto de columnas de texto.
type: docs
weight: 420
url: /es/net/aspose.words/pagesetup/textcolumns/
---
## PageSetup.TextColumns property

Devuelve una colección que representa el conjunto de columnas de texto.

```csharp
public TextColumnCollection TextColumns { get; }
```

### Ejemplos

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

* class [TextColumnCollection](../../textcolumncollection/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../pagesetup/)
* asamblea [Aspose.Words](../../../)


