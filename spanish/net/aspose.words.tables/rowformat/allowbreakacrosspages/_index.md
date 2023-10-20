---
title: RowFormat.AllowBreakAcrossPages
linktitle: AllowBreakAcrossPages
articleTitle: AllowBreakAcrossPages
second_title: Aspose.Words para .NET
description: RowFormat AllowBreakAcrossPages propiedad. Verdadero si se permite que el texto de una fila de la tabla se divida en un salto de página en C#.
type: docs
weight: 10
url: /es/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

Verdadero si se permite que el texto de una fila de la tabla se divida en un salto de página.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

## Ejemplos

Muestra cómo deshabilitar las filas que se dividen entre páginas para cada fila de una tabla.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Establece la propiedad "AllowBreakAcrossPages" en "false" para mantener la fila
// en una sola pieza si una tabla abarca dos páginas, que se dividen a lo largo de esa fila.
// Si la fila es demasiado grande para caber en una página, Microsoft Word la empujará a la página siguiente.
// Establece la propiedad "AllowBreakAcrossPages" en "true" para permitir que la fila se divida en dos páginas.
foreach (Row row in table.OfType<Row>())
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### Ver también

* class [RowFormat](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
