---
title: Table.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words para .NET
description: Table VerticalAnchor propiedad. Obtiene el objeto base a partir del cual se debe calcular el posicionamiento vertical de la tabla flotante. El valor predeterminado esMargin  en C#.
type: docs
weight: 340
url: /es/net/aspose.words.tables/table/verticalanchor/
---
## Table.VerticalAnchor property

Obtiene el objeto base a partir del cual se debe calcular el posicionamiento vertical de la tabla flotante. El valor predeterminado esMargin .

```csharp
public RelativeVerticalPosition VerticalAnchor { get; set; }
```

## Ejemplos

Muestra cómo trabajar con propiedades de tablas flotantes.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // Solo Margen, Página y Columna están disponibles en RelativeHorizontalPosition para el configurador HorizontalAnchor.
    // Se lanzará ArgumentException para cualquier otro valor.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Solo Margen, Página y Párrafo están disponibles en RelativeVerticalPosition para el configurador VerticalAnchor.
    // Se lanzará ArgumentException para cualquier otro valor.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Ver también

* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
