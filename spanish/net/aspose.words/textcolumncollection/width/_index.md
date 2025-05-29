---
title: TextColumnCollection.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words para .NET
description: Descubra la propiedad Ancho de TextColumnCollection. Gestione fácilmente columnas con espaciado uniforme para optimizar el diseño de sus proyectos.
type: docs
weight: 60
url: /es/net/aspose.words/textcolumncollection/width/
---
## TextColumnCollection.Width property

Cuando las columnas están espaciadas uniformemente, obtiene el ancho de las columnas.

```csharp
public double Width { get; }
```

## Observaciones

Tiene efecto sólo cuando[`EvenlySpaced`](../evenlyspaced/) está configurado para`verdadero`.

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
