---
title: ChartSeries.SeriesType
linktitle: SeriesType
articleTitle: SeriesType
second_title: Aspose.Words for .NET
description: ChartSeries SeriesType property. Gets the type of this chart series in C#.
type: docs
weight: 120
url: /net/aspose.words.drawing.charts/chartseries/seriestype/
---
## ChartSeries.SeriesType property

Gets the type of this chart series.

```csharp
public ChartSeriesType SeriesType { get; }
```

## Examples

Shows how to

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Remove all series of the Column type.
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

### See Also

* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeries](../)
* namespace [Aspose.Words.Drawing.Charts](../../chartseries/)
* assembly [Aspose.Words](../../../)
