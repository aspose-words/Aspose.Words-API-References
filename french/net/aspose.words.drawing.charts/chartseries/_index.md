---
title: ChartSeries
second_title: Référence de l'API Aspose.Words pour .NET
description: Représente les propriétés de la série de graphiques.
type: docs
weight: 730
url: /fr/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

Représente les propriétés de la série de graphiques.

```csharp
public class ChartSeries : IChartDataPoint
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } |  |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | Spécifie les paramètres des étiquettes de données pour toute la série. |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | Renvoie une collection d'objets de mise en forme pour tous les points de données de cette série. |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } |  |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | Fournit un accès au remplissage et à la mise en forme des lignes de la série. |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | Obtient ou définit un indicateur indiquant si les étiquettes de données sont affichées pour la série. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } |  |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | Obtient une entrée de légende pour cette série de graphiques. |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } |  |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | Obtient ou définit le nom de la série, si le nom n'est pas défini explicitement, il est généré à l'aide de l'index. Par défaut, renvoie la série plus un index basé. |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | Permet de spécifier si la ligne reliant les points sur le graphique doit être lissée à l'aide de splines Catmull-Rom. |

### Exemples

Montre comment appliquer des étiquettes aux points de données dans un graphique en courbes.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape chartShape = builder.InsertChart(ChartType.Line, 400, 300);
    Chart chart = chartShape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // Appliquez des étiquettes de données à chaque série du graphique.
    // Ces étiquettes apparaîtront à côté de chaque point de données dans le graphique et afficheront sa valeur.
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.AreEqual(4, series.DataLabels.Count);
    }

    // Modifie la chaîne de séparation pour chaque étiquette de données d'une série.
    using (IEnumerator<ChartDataLabel> enumerator = chart.Series[0].DataLabels.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.AreEqual(", ", enumerator.Current.Separator);
            enumerator.Current.Separator = " & ";
        }
    }

    // Pour un graphique plus propre, nous pouvons supprimer les étiquettes de données individuellement.
    chart.Series[1].DataLabels[2].ClearFormat();

    // Nous pouvons également supprimer une série entière de ses étiquettes de données à la fois.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Appliquez des étiquettes de données avec un format de nombre et un séparateur personnalisés à plusieurs points de données d'une série.
/// </summary>
private static void ApplyDataLabels(ChartSeries series, int labelsCount, string numberFormat, string separator)
{
    for (int i = 0; i < labelsCount; i++)
    {
        series.HasDataLabels = true;

        Assert.False(series.DataLabels[i].IsVisible);

        series.DataLabels[i].ShowCategoryName = true;
        series.DataLabels[i].ShowSeriesName = true;
        series.DataLabels[i].ShowValue = true;
        series.DataLabels[i].ShowLeaderLines = true;
        series.DataLabels[i].ShowLegendKey = true;
        series.DataLabels[i].ShowPercentage = false;
        series.DataLabels[i].IsHidden = false;
        Assert.False(series.DataLabels[i].ShowDataLabelsRange);

        series.DataLabels[i].NumberFormat.FormatCode = numberFormat;
        series.DataLabels[i].Separator = separator;

        Assert.False(series.DataLabels[i].ShowDataLabelsRange);
        Assert.True(series.DataLabels[i].IsVisible);
        Assert.False(series.DataLabels[i].IsHidden);
    }
}
```

### Voir également

* interface [IChartDataPoint](../ichartdatapoint/)
* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
