---
title: Chart.SeriesGroups
linktitle: SeriesGroups
articleTitle: SeriesGroups
second_title: Aspose.Words para .NET
description: Explore la propiedad SeriesGroups del gráfico para acceder fácilmente a una amplia colección de grupos de series, mejorando su experiencia de visualización de datos.
type: docs
weight: 90
url: /es/net/aspose.words.drawing.charts/chart/seriesgroups/
---
## Chart.SeriesGroups property

Proporciona acceso a una colección de grupos de series de este gráfico.

```csharp
public ChartSeriesGroupCollection SeriesGroups { get; }
```

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

* class [ChartSeriesGroupCollection](../../chartseriesgroupcollection/)
* class [Chart](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
