---
title: ChartSeries.SeriesType
second_title: Aspose.Words für .NET-API-Referenz
description: ChartSeries eigendom. Ruft den Typ dieser Diagrammreihe ab.
type: docs
weight: 120
url: /de/net/aspose.words.drawing.charts/chartseries/seriestype/
---
## ChartSeries.SeriesType property

Ruft den Typ dieser Diagrammreihe ab.

```csharp
public ChartSeriesType SeriesType { get; }
```

### Beispiele

Zeigt, wie es geht

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Alle Serien vom Typ Column entfernen.
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

### Siehe auch

* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeries](../)
* namensraum [Aspose.Words.Drawing.Charts](../../chartseries/)
* Montage [Aspose.Words](../../../)


