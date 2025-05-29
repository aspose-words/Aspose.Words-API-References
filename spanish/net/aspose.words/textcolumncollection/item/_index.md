---
title: TextColumnCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words para .NET
description: Acceda a una columna de texto específica por índice con la propiedad TextColumnCollection Item. Simplifique la gestión de datos y mejore la eficiencia de su codificación.
type: docs
weight: 30
url: /es/net/aspose.words/textcolumncollection/item/
---
## TextColumnCollection indexer

Devuelve una columna de texto en el índice especificado.

```csharp
public TextColumn this[int index] { get; }
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

* class [TextColumn](../../textcolumn/)
* class [TextColumnCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
