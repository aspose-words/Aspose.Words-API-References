---
title: ChartSeries.SeriesType
second_title: Aspose.Words for .NET API Referansı
description: ChartSeries mülk. Bu grafik serisinin türünü alır.
type: docs
weight: 120
url: /tr/net/aspose.words.drawing.charts/chartseries/seriestype/
---
## ChartSeries.SeriesType property

Bu grafik serisinin türünü alır.

```csharp
public ChartSeriesType SeriesType { get; }
```

### Örnekler

Nasıl yapılacağını gösterir

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Sütun tipindeki tüm serileri kaldırın.
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

### Ayrıca bakınız

* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeries](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartseries/)
* toplantı [Aspose.Words](../../../)


