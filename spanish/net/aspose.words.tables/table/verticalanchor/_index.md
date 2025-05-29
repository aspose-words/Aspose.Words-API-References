---
title: Table.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words para .NET
description: Descubra la propiedad Table VerticalAnchor para optimizar el posicionamiento de tablas flotantes. Aprenda a mejorar el control del diseño con su valor predeterminado de Margen.
type: docs
weight: 340
url: /es/net/aspose.words.tables/table/verticalanchor/
---
## Table.VerticalAnchor property

Obtiene el objeto base desde el cual se debe calcular el posicionamiento vertical de la tabla flotante. El valor predeterminado esMargin .

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

    // Solo Margen, Página, Columna están disponibles en RelativeHorizontalPosition para el configurador HorizontalAnchor.
    // La ArgumentException se lanzará para cualquier otro valor.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Solo están disponibles Margen, Página y Párrafo en RelativeVerticalPosition para el configurador VerticalAnchor.
    // La ArgumentException se lanzará para cualquier otro valor.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Ver también

* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
