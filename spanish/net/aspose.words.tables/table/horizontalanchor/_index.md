---
title: Table.HorizontalAnchor
second_title: Referencia de API de Aspose.Words para .NET
description: Table propiedad. Obtiene el objeto base a partir del cual se debe calcular la posición horizontal de la tabla flotante. El valor predeterminado esColumn .
type: docs
weight: 170
url: /es/net/aspose.words.tables/table/horizontalanchor/
---
## Table.HorizontalAnchor property

Obtiene el objeto base a partir del cual se debe calcular la posición horizontal de la tabla flotante. El valor predeterminado esColumn .

```csharp
public RelativeHorizontalPosition HorizontalAnchor { get; set; }
```

### Ejemplos

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

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../table/)
* asamblea [Aspose.Words](../../../)


