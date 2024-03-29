---
title: Table.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words para .NET
description: Table AllowOverlap propiedad. Obtiene si una tabla flotante permitirá que otros objetos flotantes en el documento se superpongan en sus extensiones cuando se muestre. El valor predeterminado esverdadero  en C#.
type: docs
weight: 70
url: /es/net/aspose.words.tables/table/allowoverlap/
---
## Table.AllowOverlap property

Obtiene si una tabla flotante permitirá que otros objetos flotantes en el documento se superpongan en sus extensiones cuando se muestre. El valor predeterminado es`verdadero` .

```csharp
public bool AllowOverlap { get; }
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

* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
