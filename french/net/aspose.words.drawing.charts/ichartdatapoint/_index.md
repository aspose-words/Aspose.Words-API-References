---
title: IChartDataPoint Interface
linktitle: IChartDataPoint
articleTitle: IChartDataPoint
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.IChartDataPoint interface. Contient les propriétés dun seul point de données sur le graphique en C#.
type: docs
weight: 900
url: /fr/net/aspose.words.drawing.charts/ichartdatapoint/
---
## IChartDataPoint interface

Contient les propriétés d'un seul point de données sur le graphique.

```csharp
public interface IChartDataPoint
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/ichartdatapoint/bubble3d/) { get; set; } | Spécifie si les bulles du graphique à bulles doivent avoir un effet 3D appliqué. |
| [Explosion](../../aspose.words.drawing.charts/ichartdatapoint/explosion/) { get; set; } | Spécifie la distance à laquelle le point de données doit être déplacé du centre du secteur. Peut être négatif, négatif signifie que la propriété n'est pas définie et qu'aucune explosion ne doit être appliquée. S'applique uniquement aux diagrammes circulaires. |
| [InvertIfNegative](../../aspose.words.drawing.charts/ichartdatapoint/invertifnegative/) { get; set; } | Spécifie si l'élément parent doit inverser ses couleurs si la valeur est négative. |
| [Marker](../../aspose.words.drawing.charts/ichartdatapoint/marker/) { get; } | Spécifie un marqueur de données. Le marqueur est automatiquement créé sur demande. |

## Exemples

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

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
