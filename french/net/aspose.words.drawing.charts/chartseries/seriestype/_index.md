---
title: ChartSeries.SeriesType
second_title: Référence de l'API Aspose.Words pour .NET
description: ChartSeries propriété. Obtient le type de cette série de graphiques.
type: docs
weight: 120
url: /fr/net/aspose.words.drawing.charts/chartseries/seriestype/
---
## ChartSeries.SeriesType property

Obtient le type de cette série de graphiques.

```csharp
public ChartSeriesType SeriesType { get; }
```

### Exemples

Montre comment

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Supprime toutes les séries du type Column.
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

### Voir également

* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeries](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../chartseries/)
* Assemblée [Aspose.Words](../../../)


