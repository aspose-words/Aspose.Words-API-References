---
title: Table.HorizontalAnchor
linktitle: HorizontalAnchor
articleTitle: HorizontalAnchor
second_title: Aspose.Words para .NET
description: Descubra la propiedad Table HorizontalAnchor para optimizar el posicionamiento de tablas flotantes. Personalice fácilmente la alineación horizontal para un mejor control del diseño.
type: docs
weight: 170
url: /es/net/aspose.words.tables/table/horizontalanchor/
---
## Table.HorizontalAnchor property

Obtiene el objeto base desde el cual se debe calcular el posicionamiento horizontal de la tabla flotante. El valor predeterminado esColumn .

```csharp
public RelativeHorizontalPosition HorizontalAnchor { get; set; }
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

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
