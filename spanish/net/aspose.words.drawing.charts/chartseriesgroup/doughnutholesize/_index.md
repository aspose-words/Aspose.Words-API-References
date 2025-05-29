---
title: ChartSeriesGroup.DoughnutHoleSize
linktitle: DoughnutHoleSize
articleTitle: DoughnutHoleSize
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartSeriesGroup DoughnutHoleSize para personalizar fácilmente el porcentaje del tamaño del orificio de su gráfico de anillos para una mejor visualización de datos.
type: docs
weight: 50
url: /es/net/aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/
---
## ChartSeriesGroup.DoughnutHoleSize property

Obtiene o establece el tamaño del orificio del gráfico de anillos principal como un porcentaje.

```csharp
public int DoughnutHoleSize { get; set; }
```

## Observaciones

Se aplica únicamente a grupos de series de laDoughnut tipo.

El rango de valores aceptables va de 0 a 90 inclusive. El valor predeterminado es 75.

## Ejemplos

Muestra cómo crear y dar formato a un gráfico de anillos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Doughnut, 400, 400);
Chart chart = shape.Chart;
//Eliminar la serie generada por defecto.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
chart.Series.Add("Series 1", categories, new double[] { 4, 2, 5 });

// Formatear el gráfico de anillos.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.DoughnutHoleSize = 10;
seriesGroup.FirstSliceAngle = 270;

doc.Save(ArtifactsDir + "Charts.DoughnutChart.docx");
```

### Ver también

* class [ChartSeriesGroup](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
