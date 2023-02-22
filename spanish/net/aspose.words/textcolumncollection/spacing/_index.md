---
title: TextColumnCollection.Spacing
second_title: Referencia de API de Aspose.Words para .NET
description: TextColumnCollection propiedad. Cuando las columnas están espaciadas uniformemente obtiene o establece la cantidad de espacio entre cada columna en puntos.
type: docs
weight: 50
url: /es/net/aspose.words/textcolumncollection/spacing/
---
## TextColumnCollection.Spacing property

Cuando las columnas están espaciadas uniformemente, obtiene o establece la cantidad de espacio entre cada columna en puntos.

```csharp
public double Spacing { get; set; }
```

### Observaciones

Solo tiene efecto cuando[`EvenlySpaced`](../evenlyspaced/) se establece en **verdadero** .

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

* class [TextColumnCollection](../)
* espacio de nombres [Aspose.Words](../../textcolumncollection/)
* asamblea [Aspose.Words](../../../)


