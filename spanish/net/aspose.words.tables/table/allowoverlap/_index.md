---
title: Table.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words para .NET
description: Descubra la propiedad AllowOverlap de tabla, que controla si los objetos flotantes pueden superponerse a su tabla. Mejore la flexibilidad del diseño para una mejor presentación del documento.
type: docs
weight: 70
url: /es/net/aspose.words.tables/table/allowoverlap/
---
## Table.AllowOverlap property

Obtiene si una tabla flotante debe permitir que otros objetos flotantes en el documento se superpongan a sus extensiones cuando se muestran. El valor predeterminado es`verdadero` .

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

    // Solo Margen, Página, Columna están disponibles en RelativeHorizontalPosition para el configurador HorizontalAnchor.
    // La ArgumentException se lanzará para cualquier otro valor.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Solo están disponibles Margen, Página y Párrafo en RelativeVerticalPosition para el configurador VerticalAnchor.
    // La ArgumentException se lanzará para cualquier otro valor.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Ver también

* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
