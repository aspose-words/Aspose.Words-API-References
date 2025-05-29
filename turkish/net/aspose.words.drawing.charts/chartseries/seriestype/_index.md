---
title: ChartSeries.SeriesType
linktitle: SeriesType
articleTitle: SeriesType
second_title: .NET için Aspose.Words
description: Grafik serinizin türünü kolayca belirlemek ve veri görselleştirmenizi geliştirmek için ChartSeries SeriesType özelliğini keşfedin. Bugün güçlü içgörülerin kilidini açın!
type: docs
weight: 120
url: /tr/net/aspose.words.drawing.charts/chartseries/seriestype/
---
## ChartSeries.SeriesType property

Bu grafik serisinin türünü alır.

```csharp
public ChartSeriesType SeriesType { get; }
```

## Örnekler

Belirli grafik serilerinin nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Sütun türündeki tüm serileri kaldır.
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
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
