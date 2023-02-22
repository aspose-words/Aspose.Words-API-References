---
title: ChartDataLabelCollection.GetEnumerator
second_title: Référence de l'API Aspose.Words pour .NET
description: ChartDataLabelCollection méthode. Renvoie un objet énumérateur.
type: docs
weight: 140
url: /fr/net/aspose.words.drawing.charts/chartdatalabelcollection/getenumerator/
---
## ChartDataLabelCollection.GetEnumerator method

Renvoie un objet énumérateur.

```csharp
public IEnumerator<ChartDataLabel> GetEnumerator()
```

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

* class [ChartDataLabel](../../chartdatalabel/)
* class [ChartDataLabelCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection/)
* Assemblée [Aspose.Words](../../../)


