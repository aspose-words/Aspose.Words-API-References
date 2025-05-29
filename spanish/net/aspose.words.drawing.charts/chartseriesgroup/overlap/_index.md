---
title: ChartSeriesGroup.Overlap
linktitle: Overlap
articleTitle: Overlap
second_title: Aspose.Words para .NET
description: Descubra la propiedad Superposición de ChartSeriesGroup para ajustar fácilmente el porcentaje de superposición de las barras o columnas de su serie para una mejor visualización de datos.
type: docs
weight: 80
url: /es/net/aspose.words.drawing.charts/chartseriesgroup/overlap/
---
## ChartSeriesGroup.Overlap property

Obtiene o establece el porcentaje de superposición de las barras o columnas de la serie.

```csharp
public int Overlap { get; set; }
```

## Observaciones

Se aplica a grupos de series de todos los tipos de barras y columnas.

El rango de valores aceptables va de -100 a 100 inclusive. Un valor de 0 indica que no hay espacio entre barras/columnas. Si el valor es -100, la distancia entre barras/columnas es igual a su ancho. Un valor de 100 significa que las barras/columnas se superponen completamente.

## Ejemplos

Muestra cómo configurar el ancho del espacio y la superposición.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// Establezca el ancho del espacio entre columnas y la superposición.
seriesGroup.GapWidth = 450;
seriesGroup.Overlap = -75;

doc.Save(ArtifactsDir + "Charts.ConfigureGapOverlap.docx");
```

### Ver también

* class [ChartSeriesGroup](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
