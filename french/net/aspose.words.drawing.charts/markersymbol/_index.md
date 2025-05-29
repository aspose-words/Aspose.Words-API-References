---
title: MarkerSymbol Enum
linktitle: MarkerSymbol
articleTitle: MarkerSymbol
second_title: Aspose.Words pour .NET
description: Explorez l'énumération Aspose.Words.Drawing.Charts.MarkerSymbol pour des styles de marqueurs personnalisables qui améliorent les visuels de vos graphiques et améliorent la présentation des données.
type: docs
weight: 1240
url: /fr/net/aspose.words.drawing.charts/markersymbol/
---
## MarkerSymbol enumeration

Spécifie le style du symbole du marqueur.

```csharp
public enum MarkerSymbol
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Default | `0` | Spécifie qu'un symbole de marqueur par défaut doit être dessiné à chaque point de données. |
| Circle | `1` | Spécifie qu'un cercle doit être dessiné à chaque point de données. |
| Dash | `2` | Spécifie qu'un tiret doit être dessiné à chaque point de données. |
| Diamond | `3` | Spécifie qu'un losange doit être dessiné à chaque point de données. |
| Dot | `4` | Spécifie qu'un point doit être dessiné à chaque point de données. |
| None | `5` | Spécifie que rien ne doit être dessiné à chaque point de données. |
| Picture | `6` | Spécifie qu'une image doit être dessinée à chaque point de données. |
| Plus | `7` | Spécifie qu'un signe plus doit être dessiné à chaque point de données. |
| Square | `8` | Spécifie qu'un carré doit être dessiné à chaque point de données. |
| Star | `9` | Spécifie qu'une étoile doit être dessinée à chaque point de données. |
| Triangle | `10` | Spécifie qu'un triangle doit être dessiné à chaque point de données. |
| X | `11` | Spécifie qu'un X doit être dessiné à chaque point de données. |

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

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
