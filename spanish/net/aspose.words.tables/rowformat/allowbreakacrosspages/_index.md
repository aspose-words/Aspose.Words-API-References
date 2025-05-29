---
title: RowFormat.AllowBreakAcrossPages
linktitle: AllowBreakAcrossPages
articleTitle: AllowBreakAcrossPages
second_title: Aspose.Words para .NET
description: Descubra la propiedad RowFormat AllowBreakAcrossPages, que permite un flujo de texto continuo en las filas de la tabla a través de los saltos de página para mejorar la legibilidad y la presentación.
type: docs
weight: 10
url: /es/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

Verdadero si se permite que el texto de una fila de tabla se divida en un salto de página.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

## Ejemplos

Muestra cómo deshabilitar la división de filas en varias páginas para cada fila de una tabla.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Establezca la propiedad "AllowBreakAcrossPages" en "falso" para mantener la fila
// en una sola pieza si una tabla abarca dos páginas, que se dividen a lo largo de esa fila.
// Si la fila es demasiado grande para caber en una página, Microsoft Word la moverá a la página siguiente.
// Establezca la propiedad "AllowBreakAcrossPages" en "true" para permitir que la fila se divida en dos páginas.
foreach (Row row in table)
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### Ver también

* class [RowFormat](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
