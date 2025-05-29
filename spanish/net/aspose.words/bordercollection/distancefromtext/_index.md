---
title: BorderCollection.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: Aspose.Words para .NET
description: Descubre la propiedad DistanciaDesdeTexto de BorderCollection para personalizar fácilmente el espaciado del borde del texto en tus diseños. ¡Optimiza tu diseño sin esfuerzo!
type: docs
weight: 40
url: /es/net/aspose.words/bordercollection/distancefromtext/
---
## BorderCollection.DistanceFromText property

Obtiene o establece la distancia del borde desde el texto en puntos.

```csharp
public double DistanceFromText { get; set; }
```

## Observaciones

Obtiene la distancia desde el texto para el primer borde.

Establece la distancia desde el texto para todos los bordes de la colección, excluidos los bordes diagonales.

No tiene ningún efecto y se restablecerá automáticamente a cero para los bordes de las celdas de la tabla.

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
