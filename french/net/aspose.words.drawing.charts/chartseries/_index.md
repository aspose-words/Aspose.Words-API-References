---
title: Class ChartSeries
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.ChartSeries classe. Représente les propriétés de la série de graphiques.
type: docs
weight: 780
url: /fr/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

Représente les propriétés de la série de graphiques.

Pour en savoir plus, visitez le[Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) article documentaire.

```csharp
public class ChartSeries : IChartDataPoint
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } | Spécifie si les bulles du graphique à bulles doivent avoir un effet 3D appliqué. |
| [BubbleSizes](../../aspose.words.drawing.charts/chartseries/bubblesizes/) { get; } | Obtient une collection de tailles de bulles pour cette série de graphiques. |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | Spécifie les paramètres des étiquettes de données pour toute la série. |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | Renvoie une collection d'objets de formatage pour tous les points de données de cette série. |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } | Spécifie la distance à laquelle le point de données doit être déplacé du centre du secteur. Peut être négatif, négatif signifie que la propriété n'est pas définie et qu'aucune explosion ne doit être appliquée. S'applique uniquement aux diagrammes circulaires. |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | Donne accès au formatage de remplissage et de ligne de la série. |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | Obtient ou définit un indicateur indiquant si les étiquettes de données sont affichées pour la série. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } | Spécifie si l'élément parent doit inverser ses couleurs si la valeur est négative. |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | Obtient une entrée de légende pour cette série de graphiques. |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } | Spécifie un marqueur de données. Le marqueur est automatiquement créé sur demande. |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | Obtient ou définit le nom de la série, si le nom n'est pas défini explicitement, il est généré à l'aide de index. Par défaut, renvoie la série plus un index basé. |
| [SeriesType](../../aspose.words.drawing.charts/chartseries/seriestype/) { get; } | Obtient le type de cette série de graphiques. |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | Permet de spécifier si la ligne reliant les points sur le graphique doit être lissée à l'aide des splines Catmull-Rom. |
| [XValues](../../aspose.words.drawing.charts/chartseries/xvalues/) { get; } | Obtient une collection de valeurs X pour cette série de graphiques. |
| [YValues](../../aspose.words.drawing.charts/chartseries/yvalues/) { get; } | Obtient une collection de valeurs Y pour cette série de graphiques. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add)(ChartXValue) | Ajoute la valeur X spécifiée à la série de graphiques. Si la série prend en charge les valeurs Y et les tailles de bulles, elles seront vides pour la valeur X. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_1)(ChartXValue, ChartYValue) | Ajoute les valeurs X et Y spécifiées à la série de graphiques. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_2)(ChartXValue, ChartYValue, double) | Ajoute la valeur X, la valeur Y et la taille de bulle spécifiées à la série de graphiques. |
| [Clear](../../aspose.words.drawing.charts/chartseries/clear/)() | Supprime toutes les valeurs de données de la série de graphiques. Le format de tous les points de données individuels et étiquettes de données est effacé. |
| [ClearValues](../../aspose.words.drawing.charts/chartseries/clearvalues/)() | Supprime toutes les valeurs de données de la série de graphiques en préservant le format des points de données et des étiquettes de données. |
| [CopyFormatFrom](../../aspose.words.drawing.charts/chartseries/copyformatfrom/)(int) |  |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert)(int, ChartXValue) | Insère la valeur X spécifiée dans la série de graphiques à l'index spécifié. Si la série prend en charge les valeurs Y et les tailles de bulles, elles seront vides pour la valeur X. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_1)(int, ChartXValue, ChartYValue) | Insère les valeurs X et Y spécifiées dans la série de graphiques à l'index spécifié. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_2)(int, ChartXValue, ChartYValue, double) | Insère la valeur X, la valeur Y et la taille de bulle spécifiées dans la série de graphiques à l'index spécifié. |
| [Remove](../../aspose.words.drawing.charts/chartseries/remove/)(int) | Supprime la valeur X, la valeur Y et la taille de la bulle, si prises en charge, de la série de graphiques à l'index spécifié. Le point de données et l'étiquette de données correspondants sont également supprimés. |

### Exemples

Montre comment appliquer des étiquettes aux points de données dans un graphique linéaire.

```csharp
public void DataLabels()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape chartShape = builder.InsertChart(ChartType.Line, 400, 300);
    Chart chart = chartShape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // Applique des étiquettes de données à chaque série du graphique.
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
/// Appliquez des étiquettes de données avec un format numérique personnalisé et un séparateur à plusieurs points de données d'une série.
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


