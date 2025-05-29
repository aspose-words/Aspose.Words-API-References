---
title: ChartDataPoint Class
linktitle: ChartDataPoint
articleTitle: ChartDataPoint
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.Charts.ChartDataPoint pour formater facilement des points de données de graphique individuels, améliorant ainsi la visualisation de vos données avec précision.
type: docs
weight: 970
url: /fr/net/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class

Permet de spécifier la mise en forme d'un seul point de données sur le graphique.

Pour en savoir plus, visitez le[Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) article de documentation.

```csharp
public class ChartDataPoint : IChartDataPoint
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartdatapoint/bubble3d/) { get; set; } | Spécifie si les bulles du graphique à bulles doivent avoir un effet 3D appliqué. |
| [Explosion](../../aspose.words.drawing.charts/chartdatapoint/explosion/) { get; set; } | Spécifie la quantité de déplacement du point de données par rapport au centre du graphique à secteurs. Peut être négatif, ce qui signifie que la propriété n'est pas définie et qu'aucune explosion ne doit être appliquée. S'applique uniquement aux graphiques à secteurs. |
| [Format](../../aspose.words.drawing.charts/chartdatapoint/format/) { get; } | Fournit l'accès au remplissage et au formatage des lignes de ce point de données. |
| [Index](../../aspose.words.drawing.charts/chartdatapoint/index/) { get; } | Index du point de données auquel cet objet applique la mise en forme. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartdatapoint/invertifnegative/) { get; set; } | Spécifie si l'élément parent doit inverser ses couleurs si la valeur est négative. |
| [Marker](../../aspose.words.drawing.charts/chartdatapoint/marker/) { get; } | Spécifie le marqueur de données du graphique. |

## Méthodes

| Nom | La description |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapoint/clearformat/)() | Efface le format de ce point de données. Les propriétés sont définies sur les valeurs par défaut définies dans la série parente. |

## Remarques

Sur une série, le`ChartDataPoint` l'objet est un membre du[`ChartDataPointCollection`](../chartdatapointcollection/) . Le[`ChartDataPointCollection`](../chartdatapointcollection/) contient un`ChartDataPoint` objet pour chaque point.

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

* interface [IChartDataPoint](../ichartdatapoint/)
* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
