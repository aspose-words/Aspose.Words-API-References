---
title: ChartSeries.SeriesType
linktitle: SeriesType
articleTitle: SeriesType
second_title: Aspose.Words för .NET
description: ChartSeries SeriesType fast egendom. Hämtar typen av denna diagramserie i C#.
type: docs
weight: 120
url: /sv/net/aspose.words.drawing.charts/chartseries/seriestype/
---
## ChartSeries.SeriesType property

Hämtar typen av denna diagramserie.

```csharp
public ChartSeriesType SeriesType { get; }
```

## Exempel

Visar hur man

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Ta bort alla serier av kolumntypen.
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

### Se även

* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeries](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
