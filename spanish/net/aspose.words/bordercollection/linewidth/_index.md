---
title: BorderCollection.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words para .NET
description: Descubra la propiedad LineWidth de BorderCollection para ajustar fácilmente el ancho del borde en puntos, mejorando la precisión y el atractivo visual de su diseño.
type: docs
weight: 90
url: /es/net/aspose.words/bordercollection/linewidth/
---
## BorderCollection.LineWidth property

Obtiene o establece el ancho del borde en puntos.

```csharp
public double LineWidth { get; set; }
```

## Observaciones

Devuelve el ancho del primer borde de la colección.

Establece el ancho de todos los bordes de la colección, excluidos los bordes diagonales.

## Ejemplos

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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
