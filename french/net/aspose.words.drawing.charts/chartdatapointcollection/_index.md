---
title: Class ChartDataPointCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.ChartDataPointCollection classe. Représente la collection dunChartDataPoint .
type: docs
weight: 700
url: /fr/net/aspose.words.drawing.charts/chartdatapointcollection/
---
## ChartDataPointCollection class

Représente la collection d'un[`ChartDataPoint`](../chartdatapoint/) .

Pour en savoir plus, visitez le[Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) article documentaire.

```csharp
public class ChartDataPointCollection : IEnumerable<ChartDataPoint>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatapointcollection/count/) { get; } | Renvoie le nombre de[`ChartDataPoint`](../chartdatapoint/) dans cette collection. |
| [Item](../../aspose.words.drawing.charts/chartdatapointcollection/item/) { get; } | Retours[`ChartDataPoint`](../chartdatapoint/) pour l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapointcollection/clearformat/)() | Efface le format de tous[`ChartDataPoint`](../chartdatapoint/) dans cette collection. |
| [CopyFormat](../../aspose.words.drawing.charts/chartdatapointcollection/copyformat/)(int, int) |  |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatapointcollection/getenumerator/)() | Renvoie un objet énumérateur. |
| [HasDefaultFormat](../../aspose.words.drawing.charts/chartdatapointcollection/hasdefaultformat/)(int) |  |

### Exemples

Montre comment utiliser des points de données sur un graphique linéaire.

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

    // Accentue les points de données du graphique en les faisant apparaître sous forme de losange.
    foreach (ChartSeries series in chart.Series) 
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // Lisse la ligne qui représente la première série de données.
    chart.Series[0].Smooth = true;

    // Vérifiez que les points de données de la première série n'inverseront pas leurs couleurs si la valeur est négative.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    // Pour un graphique plus propre, nous pouvons effacer le format individuellement.
    chart.Series[1].DataPoints[2].ClearFormat();

    // Nous pouvons également supprimer toute une série de points de données à la fois.
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

* class [ChartDataPoint](../chartdatapoint/)
* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)


