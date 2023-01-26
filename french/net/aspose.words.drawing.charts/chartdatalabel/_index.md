---
title: ChartDataLabel
second_title: Référence de l'API Aspose.Words pour .NET
description: Représente une étiquette de données sur un point de graphique ou une ligne de tendance.
type: docs
weight: 630
url: /fr/net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

Représente une étiquette de données sur un point de graphique ou une ligne de tendance.

```csharp
public class ChartDataLabel
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index/) { get; } | Spécifie l'index de l'élément conteneur. Cet index doit déterminer à quelle collection d'enfants du parent cet élément s'applique. La valeur par défaut est 0. |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden/) { get; set; } | Obtient/définit un indicateur indiquant si cette étiquette est masquée. La valeur par défaut est **faux** . |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible/) { get; } | Renvoie vrai si cette étiquette de données a quelque chose à afficher. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat/) { get; } | Renvoie le format numérique de l'élément parent. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator/) { get; set; } | Obtient ou définit le séparateur de chaîne utilisé pour les étiquettes de données sur un graphique. La valeur par défaut est une virgule, sauf pour les graphiques circulaires affichant uniquement le nom de la catégorie et le pourcentage, lorsqu'un saut de ligne doit être utilisé à la place. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize/) { get; set; } | Permet de spécifier si la taille des bulles doit être affichée pour les étiquettes de données sur un graphique. S'applique uniquement aux graphiques à bulles. La valeur par défaut est false. |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname/) { get; set; } | Permet de spécifier si le nom de la catégorie doit être affiché pour les étiquettes de données sur un graphique. La valeur par défaut est false. |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/) { get; set; } | Permet de spécifier si les valeurs des étiquettes de données doivent être affichées dans les étiquettes de données. La valeur par défaut est false. |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines/) { get; set; } | Permet de spécifier si les lignes de repère des étiquettes de données doivent être affichées. La valeur par défaut est false. |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey/) { get; set; } | Permet de spécifier si la clé de légende doit être affichée pour les étiquettes de données sur un graphique. La valeur par défaut est false. |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage/) { get; set; } | Permet de spécifier si la valeur en pourcentage doit être affichée pour les étiquettes de données sur un graphique. La valeur par défaut est false. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname/) { get; set; } | Renvoie ou définit un booléen pour indiquer le comportement d'affichage du nom de la série pour les étiquettes de données sur un graphique. True pour afficher le nom de la série. Faux pour cacher. Par défaut faux. |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue/) { get; set; } | Permet de spécifier si les valeurs doivent être affichées dans les étiquettes de données. La valeur par défaut est false. |

## Méthodes

| Nom | La description |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat/)() | Efface le format de cette étiquette de données. Les propriétés sont définies sur les valeurs par défaut définies dans la collection d'étiquettes data parent. |

### Remarques

Sur une série, le`ChartDataLabel` l'objet est membre du[`ChartDataLabelCollection`](../chartdatalabelcollection/) . Le[`ChartDataLabelCollection`](../chartdatalabelcollection/) contient un`ChartDataLabel` objet pour chaque point.

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

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
