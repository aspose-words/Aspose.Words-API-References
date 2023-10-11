---
title: ChartSeries.SeriesType
second_title: Aspose.Words per .NET API Reference
description: ChartSeries proprietà. Ottiene il tipo di questa serie di grafici.
type: docs
weight: 120
url: /it/net/aspose.words.drawing.charts/chartseries/seriestype/
---
## ChartSeries.SeriesType property

Ottiene il tipo di questa serie di grafici.

```csharp
public ChartSeriesType SeriesType { get; }
```

### Esempi

Mostra come

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Rimuove tutte le serie del tipo Colonna.
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

### Guarda anche

* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeries](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../chartseries/)
* assemblea [Aspose.Words](../../../)


