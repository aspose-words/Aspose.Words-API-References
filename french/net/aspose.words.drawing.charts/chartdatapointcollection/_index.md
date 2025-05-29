---
title: ChartDataPointCollection Class
linktitle: ChartDataPointCollection
articleTitle: ChartDataPointCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.Charts.ChartDataPointCollection, votre clé pour gérer sans effort les collections ChartDataPoint pour une visualisation améliorée des données.
type: docs
weight: 980
url: /fr/net/aspose.words.drawing.charts/chartdatapointcollection/
---
## ChartDataPointCollection class

Représente une collection d'un[`ChartDataPoint`](../chartdatapoint/) .

Pour en savoir plus, visitez le[Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) article de documentation.

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
| [CopyFormat](../../aspose.words.drawing.charts/chartdatapointcollection/copyformat/)(*int, int*) | Copie le format du point de données source vers le point de données de destination. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatapointcollection/getenumerator/)() | Renvoie un objet énumérateur. |
| [HasDefaultFormat](../../aspose.words.drawing.charts/chartdatapointcollection/hasdefaultformat/)(*int*) | Obtient un indicateur indiquant si le point de données à l'index spécifié a un format par défaut. |

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

* class [ChartDataPoint](../chartdatapoint/)
* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
