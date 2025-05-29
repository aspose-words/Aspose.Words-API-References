---
title: ChartDataLabel.ShowSeriesName
linktitle: ShowSeriesName
articleTitle: ShowSeriesName
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShowSeriesName de ChartDataLabel pour contrôler facilement la visibilité des noms de séries sur vos graphiques. Améliorez la clarté des données grâce à un simple paramètre booléen !
type: docs
weight: 190
url: /fr/net/aspose.words.drawing.charts/chartdatalabel/showseriesname/
---
## ChartDataLabel.ShowSeriesName property

Renvoie ou définit une valeur booléenne pour indiquer le comportement d'affichage du nom de la série pour les étiquettes de données sur un graphique. `vrai` pour afficher le nom de la série ;`FAUX` pour masquer. Par défaut`FAUX` .

```csharp
public bool ShowSeriesName { get; set; }
```

## Exemples

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

    // Appliquer des étiquettes de données à chaque série du graphique.
    // Ces étiquettes apparaîtront à côté de chaque point de données dans le graphique et afficheront sa valeur.
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.AreEqual(4, series.DataLabels.Count);
    }

    // Modifiez la chaîne de séparation pour chaque étiquette de données d'une série.
    using (IEnumerator<ChartDataLabel> enumerator = chart.Series[0].DataLabels.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.AreEqual(", ", enumerator.Current.Separator);
            enumerator.Current.Separator = " & ";
        }
    }

    ChartDataLabel dataLabel = chart.Series[1].DataLabels[2];
    dataLabel.Format.Fill.Color = Color.Red;

    // Pour un graphique plus propre, nous pouvons supprimer les étiquettes de données individuellement.
    dataLabel.ClearFormat();

    // Nous pouvons également supprimer une série entière de ses étiquettes de données à la fois.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Appliquez des étiquettes de données avec un format numérique personnalisé et un séparateur à plusieurs points de données d'une série.
/// </summary>
private static void ApplyDataLabels(ChartSeries series, int labelsCount, string numberFormat, string separator)
{
    series.HasDataLabels = true;
    series.Explosion = 40;

    for (int i = 0; i < labelsCount; i++)
    {
        Assert.False(series.DataLabels[i].IsVisible);

        series.DataLabels[i].ShowCategoryName = true;
        series.DataLabels[i].ShowSeriesName = true;
        series.DataLabels[i].ShowValue = true;
        series.DataLabels[i].ShowLeaderLines = true;
        series.DataLabels[i].ShowLegendKey = true;
        series.DataLabels[i].ShowPercentage = false;
        Assert.False(series.DataLabels[i].IsHidden);
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

* class [ChartDataLabel](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
