---
title: TextColumnCollection.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words para .NET
description: Descubra la propiedad Espaciado de TextColumnCollection y administre fácilmente el espaciado de columnas en puntos para lograr un diseño impecable y profesional. ¡Mejore su diseño hoy mismo!
type: docs
weight: 50
url: /es/net/aspose.words/textcolumncollection/spacing/
---
## TextColumnCollection.Spacing property

Cuando las columnas están espaciadas uniformemente, obtiene o establece la cantidad de espacio entre cada columna en puntos.

```csharp
public double Spacing { get; set; }
```

## Observaciones

Tiene efecto sólo cuando[`EvenlySpaced`](../evenlyspaced/) está configurado para`verdadero` .

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
