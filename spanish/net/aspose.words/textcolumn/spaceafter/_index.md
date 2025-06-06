---
title: TextColumn.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words para .NET
description: Descubre la propiedad TextColumn SpaceAfter para ajustar fácilmente el espaciado entre columnas en tu diseño. ¡Mejora la legibilidad y diseña con precisión!
type: docs
weight: 10
url: /es/net/aspose.words/textcolumn/spaceafter/
---
## TextColumn.SpaceAfter property

Obtiene o establece el espacio entre esta columna y la siguiente en puntos. No es necesario para la última columna.

```csharp
public double SpaceAfter { get; set; }
```

## Ejemplos

Muestra cómo crear columnas con espacios desiguales.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Determinar la cantidad de espacio que tenemos disponible para organizar las columnas.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Establezca la primera columna para que sea estrecha.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Establezca la segunda columna para tomar el resto del espacio disponible dentro de los márgenes de la página.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### Ver también

* class [TextColumn](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
