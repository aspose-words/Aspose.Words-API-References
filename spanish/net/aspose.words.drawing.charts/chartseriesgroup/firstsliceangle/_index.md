---
title: ChartSeriesGroup.FirstSliceAngle
linktitle: FirstSliceAngle
articleTitle: FirstSliceAngle
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartSeriesGroup FirstSliceAngle para personalizar el ángulo del primer corte de su gráfico circular en grados para una mejor visualización de datos.
type: docs
weight: 60
url: /es/net/aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/
---
## ChartSeriesGroup.FirstSliceAngle property

Obtiene o establece el ángulo, en grados, de la primera porción del gráfico circular principal.

```csharp
public int FirstSliceAngle { get; set; }
```

## Observaciones

Se aplica a grupos de series de laPie ,Pie3D yDoughnut tipos.

El rango de valores aceptables va de 0 a 360 inclusive. El valor predeterminado es 0.

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
