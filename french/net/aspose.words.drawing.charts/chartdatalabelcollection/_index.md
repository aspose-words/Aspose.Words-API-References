---
title: Class ChartDataLabelCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.ChartDataLabelCollection classe. Représente une collection deChartDataLabel .
type: docs
weight: 640
url: /fr/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

Représente une collection de[`ChartDataLabel`](../chartdatalabel/) .

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count/) { get; } | Renvoie le nombre de[`ChartDataLabel`](../chartdatalabel/) dans cette collection. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item/) { get; } | Retours[`ChartDataLabel`](../chartdatalabel/) pour l'index spécifié. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat/) { get; } | Obtient un[`ChartNumberFormat`](../chartnumberformat/) instance permettant de définir le format des nombres pour les étiquettes de données de la série entière. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator/) { get; set; } | Obtient ou définit le séparateur de chaîne utilisé pour les étiquettes de données de la série entière. La valeur par défaut est une virgule, sauf pour les graphiques circulaires affichant uniquement le nom de la catégorie et le pourcentage, lorsqu'un saut de ligne doit être utilisé à la place. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/) { get; set; } | Permet de spécifier si la taille des bulles doit être affichée pour les étiquettes de données de toute la série. S'applique uniquement aux graphiques à bulles. La valeur par défaut est **faux** . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/) { get; set; } | Permet de spécifier si le nom de la catégorie doit être affiché pour les étiquettes de données de toute la série. La valeur par défaut est **faux** . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange/) { get; set; } | Permet de spécifier si les valeurs des étiquettes de données doivent être affichées dans les étiquettes de données de toute la série. La valeur par défaut est **faux** . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/) { get; set; } | Permet de spécifier si les lignes de repère des étiquettes de données doivent être affichées pour les étiquettes de données de la série entière. La valeur par défaut est **faux** . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/) { get; set; } | Permet de spécifier si la clé de légende doit être affichée pour les étiquettes de données de toute la série. La valeur par défaut est **faux** . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/) { get; set; } | Permet de spécifier si la valeur en pourcentage doit être affichée pour les étiquettes de données de toute la série. La valeur par défaut est **faux** . S'applique uniquement aux graphiques à secteurs. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/) { get; set; } | Renvoie ou définit un booléen pour indiquer le comportement d'affichage du nom de la série pour les étiquettes de données de la série entière.  **Vrai**pour afficher le nom de la série. **Faux** cacher. Par défaut **faux** . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue/) { get; set; } | Permet de spécifier si les valeurs doivent être affichées dans les étiquettes de données de toute la série. La valeur par défaut est **faux** . |

## Méthodes

| Nom | La description |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat/)() | Efface le format de tous[`ChartDataLabel`](../chartdatalabel/) dans cette collection. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator/)() | Renvoie un objet énumérateur. |

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

* class [ChartDataLabel](../chartdatalabel/)
* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)


