---
title: ChartSeriesGroup.GapWidth
linktitle: GapWidth
articleTitle: GapWidth
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartSeriesGroup GapWidth para ajustar fácilmente el porcentaje de espacio entre los elementos del gráfico para una mejor visualización de datos.
type: docs
weight: 70
url: /es/net/aspose.words.drawing.charts/chartseriesgroup/gapwidth/
---
## ChartSeriesGroup.GapWidth property

Obtiene o establece el porcentaje de ancho del espacio entre los elementos del gráfico.

```csharp
public int GapWidth { get; set; }
```

## Observaciones

Se aplica únicamente a grupos de series de tipos de barras, columnas, gráficos circulares de barras, gráficos circulares de tarta, histogramas, cajas y bigotes, cascadas y embudos.

El rango de valores aceptables va de 0 a 500, ambos inclusive. Para grupos de series basados en barras/columnas, la propiedad representa el espacio entre los grupos de barras como porcentaje de su ancho. Para gráficos circulares y gráficos de barras circulares , este es el espacio entre las secciones principal y secundaria del gráfico.

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
