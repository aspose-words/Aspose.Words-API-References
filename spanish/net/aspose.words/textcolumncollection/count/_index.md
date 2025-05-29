---
title: TextColumnCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words para .NET
description: Descubra la propiedad TextColumnCollection Count para acceder fácilmente al número de columnas en la sección de su documento para un mejor control del diseño.
type: docs
weight: 10
url: /es/net/aspose.words/textcolumncollection/count/
---
## TextColumnCollection.Count property

Obtiene el número de columnas en la sección de un documento.

```csharp
public int Count { get; }
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

* class [TextColumnCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
