---
title: ShapeBase.AllowOverlap
second_title: Referencia de API de Aspose.Words para .NET
description: ShapeBase propiedad. Obtiene o establece un valor que especifica si esta forma puede superponerse a otras formas.
type: docs
weight: 10
url: /es/net/aspose.words.drawing/shapebase/allowoverlap/
---
## ShapeBase.AllowOverlap property

Obtiene o establece un valor que especifica si esta forma puede superponerse a otras formas.

```csharp
public bool AllowOverlap { get; set; }
```

### Observaciones

Esta propiedad afecta el comportamiento de la forma en Microsoft Word. Aspose.Words ignora el valor de esta propiedad.

Esta propiedad solo se aplica a formas de nivel superior.

El valor predeterminado es`verdadero`.

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

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../shapebase/)
* asamblea [Aspose.Words](../../../)


