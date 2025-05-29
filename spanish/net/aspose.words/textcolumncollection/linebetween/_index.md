---
title: TextColumnCollection.LineBetween
linktitle: LineBetween
articleTitle: LineBetween
second_title: Aspose.Words para .NET
description: Mejore su diseño con la propiedad TextColumnCollection LineBetween. Active líneas verticales entre columnas para una apariencia elegante y organizada.
type: docs
weight: 40
url: /es/net/aspose.words/textcolumncollection/linebetween/
---
## TextColumnCollection.LineBetween property

Cuando`verdadero` , agrega una línea vertical entre columnas.

```csharp
public bool LineBetween { get; set; }
```

## Ejemplos

Muestra cómo separar columnas con una línea vertical.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Configure el objeto PageSetup de la sección actual para dividir el texto en varias columnas.
// Establezca la propiedad "LineBetween" en "verdadero" para colocar una línea divisoria entre las columnas.
// Establezca la propiedad "LineBetween" en "false" para dejar el espacio entre columnas en blanco.
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.LineBetween = lineBetween;
columns.SetCount(3);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 3.");

doc.Save(ArtifactsDir + "PageSetup.VerticalLineBetweenColumns.docx");
```

### Ver también

* class [TextColumnCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
