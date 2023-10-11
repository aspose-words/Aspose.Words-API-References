---
title: ChartSeries.SeriesType
second_title: Referencia de API de Aspose.Words para .NET
description: ChartSeries propiedad. Obtiene el tipo de esta serie de gráficos.
type: docs
weight: 120
url: /es/net/aspose.words.drawing.charts/chartseries/seriestype/
---
## ChartSeries.SeriesType property

Obtiene el tipo de esta serie de gráficos.

```csharp
public ChartSeriesType SeriesType { get; }
```

### Ejemplos

Muestra cómo

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Elimina todas las series del tipo Columna.
for (int i = chart.Series.Count - 1; i >= 0; i--)
{
    if (chart.Series[i].SeriesType == ChartSeriesType.Column)
        chart.Series.RemoveAt(i);
}

chart.Series.Add(
    "Aspose Series",
    new string[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 5.6, 7.1, 2.9, 8.9 });

doc.Save(ArtifactsDir + "Charts.RemoveSpecificChartSeries.docx");
```

### Ver también

* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeries](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../chartseries/)
* asamblea [Aspose.Words](../../../)


