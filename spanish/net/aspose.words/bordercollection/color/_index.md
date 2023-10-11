---
title: BorderCollection.Color
second_title: Referencia de API de Aspose.Words para .NET
description: BorderCollection propiedad. Obtiene o establece el color del borde.
type: docs
weight: 20
url: /es/net/aspose.words/bordercollection/color/
---
## BorderCollection.Color property

Obtiene o establece el color del borde.

```csharp
public Color Color { get; set; }
```

### Observaciones

Devuelve el color del primer borde de la colección.

Establece el color de todos los bordes de la colección, excepto los bordes diagonales.

### Ejemplos

Muestra cómo crear un borde de página ondulado verde con una sombra.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### Ver también

* class [BorderCollection](../)
* espacio de nombres [Aspose.Words](../../bordercollection/)
* asamblea [Aspose.Words](../../../)


