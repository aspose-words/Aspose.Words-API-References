---
title: ShapeBase.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words para .NET
description: Descubra la propiedad AllowOverlap de ShapeBase, controle las interacciones de formas habilitando o deshabilitando la superposición con otras formas para una mayor flexibilidad de diseño.
type: docs
weight: 10
url: /es/net/aspose.words.drawing/shapebase/allowoverlap/
---
## ShapeBase.AllowOverlap property

Obtiene o establece un valor que especifica si esta forma puede superponerse a otras formas.

```csharp
public bool AllowOverlap { get; set; }
```

## Observaciones

Esta propiedad afecta el comportamiento de la forma en Microsoft Word. Aspose.Words ignora el valor de esta propiedad.

Esta propiedad solo se aplica a formas de nivel superior.

El valor predeterminado es`verdadero`.

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

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
