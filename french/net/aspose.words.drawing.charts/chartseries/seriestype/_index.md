---
title: ChartSeries.SeriesType
linktitle: SeriesType
articleTitle: SeriesType
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartSeries SeriesType pour identifier facilement le type de vos séries de graphiques et améliorer la visualisation de vos données. Accédez à des informations précieuses dès aujourd'hui !
type: docs
weight: 120
url: /fr/net/aspose.words.drawing.charts/chartseries/seriestype/
---
## ChartSeries.SeriesType property

Obtient le type de cette série de graphiques.

```csharp
public ChartSeriesType SeriesType { get; }
```

## Exemples

Montre comment supprimer des séries de graphiques spécifiques.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Supprimez toutes les séries de type Colonne.
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
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
