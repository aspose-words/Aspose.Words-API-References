---
title: AllowBreakAcrossPages
second_title: Referencia de API de Aspose.Words para .NET
description: Verdadero si se permite que el texto de una fila de la tabla se divida en un salto de página.
type: docs
weight: 10
url: /es/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

Verdadero si se permite que el texto de una fila de la tabla se divida en un salto de página.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

### Ejemplos

Muestra cómo deshabilitar la separación de filas entre páginas para cada fila de una tabla.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Establecer la propiedad "AllowBreakAcrossPages" en "falso" para mantener la fila
// en una sola pieza si una tabla ocupa dos páginas, que se dividen a lo largo de esa fila.
// Si la fila es demasiado grande para caber en una página, Microsoft Word la bajará a la página siguiente.
// Establezca la propiedad "AllowBreakAcrossPages" en "true" para permitir que la fila se divida en dos páginas.
foreach (Row row in table.OfType<Row>())
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### Ver también

* class [RowFormat](../../rowformat)
* espacio de nombres [Aspose.Words.Tables](../../rowformat)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
