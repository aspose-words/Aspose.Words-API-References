---
title: IChartDataPoint.Marker
linktitle: Marker
articleTitle: Marker
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IChartDataPoint Marker, qui crée automatiquement des marqueurs de données pour une visualisation et une analyse optimisées. Optimisez votre expérience graphique !
type: docs
weight: 40
url: /fr/net/aspose.words.drawing.charts/ichartdatapoint/marker/
---
## IChartDataPoint.Marker property

Spécifie un marqueur de données. Le marqueur est créé automatiquement à la demande.

```csharp
public ChartMarker Marker { get; }
```

## Exemples

Montre comment travailler avec des points de données sur un graphique linéaire.

```csharp
public void ChartDataPoint()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape shape = builder.InsertChart(ChartType.Line, 500, 350);
    Chart chart = shape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // Mettez en valeur les points de données du graphique en les faisant apparaître sous forme de losanges.
    foreach (ChartSeries series in chart.Series)
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // Lissez la ligne qui représente la première série de données.
    chart.Series[0].Smooth = true;

    // Vérifiez que les points de données de la première série n'inverseront pas leurs couleurs si la valeur est négative.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    ChartDataPoint dataPoint = chart.Series[1].DataPoints[2];
    dataPoint.Format.Fill.Color = Color.Red;

    // Pour un graphique plus propre, nous pouvons effacer le format individuellement.
    dataPoint.ClearFormat();

    // Nous pouvons également supprimer une série entière de points de données à la fois.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// Applique un certain nombre de points de données à une série.
/// </summary>
private static void ApplyDataPoints(ChartSeries series, int dataPointsCount, MarkerSymbol markerSymbol, int dataPointSize)
{
    for (int i = 0; i < dataPointsCount; i++)
    {
        ChartDataPoint point = series.DataPoints[i];
        point.Marker.Symbol = markerSymbol;
        point.Marker.Size = dataPointSize;

        Assert.AreEqual(i, point.Index);
    }
}
```

### Voir également

* class [ChartMarker](../../chartmarker/)
* interface [IChartDataPoint](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
