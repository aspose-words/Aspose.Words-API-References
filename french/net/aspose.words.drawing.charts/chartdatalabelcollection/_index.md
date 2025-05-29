---
title: ChartDataLabelCollection Class
linktitle: ChartDataLabelCollection
articleTitle: ChartDataLabelCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.ChartDataLabelCollection pour gérer efficacement les étiquettes de données de vos graphiques. Améliorez l'attrait visuel de votre document dès aujourd'hui !
type: docs
weight: 940
url: /fr/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

Représente une collection de[`ChartDataLabel`](../chartdatalabel/) .

Pour en savoir plus, visitez le[Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) article de documentation.

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count/) { get; } | Renvoie le nombre de[`ChartDataLabel`](../chartdatalabel/) dans cette collection. |
| [Font](../../aspose.words.drawing.charts/chartdatalabelcollection/font/) { get; } | Donne accès au formatage des polices des étiquettes de données de toute la série. |
| [Format](../../aspose.words.drawing.charts/chartdatalabelcollection/format/) { get; } | Donne accès au remplissage et au formatage des lignes des étiquettes de données. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item/) { get; } | Retours[`ChartDataLabel`](../chartdatalabel/) pour l'index spécifié. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat/) { get; } | Obtient un[`ChartNumberFormat`](../chartnumberformat/) instance permettant de définir le format numérique des étiquettes de données de la série entière. |
| [Orientation](../../aspose.words.drawing.charts/chartdatalabelcollection/orientation/) { get; set; } | Obtient ou définit l'orientation du texte des étiquettes de données de la série entière. |
| [Position](../../aspose.words.drawing.charts/chartdatalabelcollection/position/) { get; set; } | Obtient ou définit la position des étiquettes de données. |
| [Rotation](../../aspose.words.drawing.charts/chartdatalabelcollection/rotation/) { get; set; } | Obtient ou définit la rotation des étiquettes de données de la série entière en degrés. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator/) { get; set; } | Obtient ou définit le séparateur de chaîne utilisé pour les étiquettes de données de la série entière. La valeur par défaut est une virgule, sauf pour les graphiques à secteurs affichant uniquement le nom de la catégorie et le pourcentage, lorsqu'un saut de ligne doit être utilisé à la place. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/) { get; set; } | Permet de spécifier si la taille des bulles doit être affichée pour les étiquettes de données de la série entière. S'applique uniquement aux graphiques à bulles. La valeur par défaut est`FAUX` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/) { get; set; } | Permet de spécifier si le nom de la catégorie doit être affiché pour les étiquettes de données de la série entière. La valeur par défaut est`FAUX` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange/) { get; set; } | Permet de spécifier si les valeurs de la plage d'étiquettes de données doivent être affichées dans les étiquettes de données de la série entière. La valeur par défaut est`FAUX` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/) { get; set; } | Permet de spécifier si les lignes de repère des étiquettes de données doivent être affichées pour les étiquettes de données de la série entière. La valeur par défaut est`FAUX` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/) { get; set; } | Permet de spécifier si la clé de légende doit être affichée pour les étiquettes de données de la série entière. La valeur par défaut est`FAUX` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/) { get; set; } | Permet de spécifier si la valeur en pourcentage doit être affichée pour les étiquettes de données de la série entière. La valeur par défaut est`FAUX` . S'applique uniquement aux graphiques à secteurs. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/) { get; set; } | Renvoie ou définit une valeur booléenne pour indiquer le comportement d'affichage du nom de la série pour les étiquettes de données de la série entière. `vrai` pour afficher le nom de la série ;`FAUX` pour masquer. Par défaut`FAUX` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue/) { get; set; } | Permet de spécifier si les valeurs doivent être affichées dans les étiquettes de données de la série entière. La valeur par défaut est`FAUX` . |

## Méthodes

| Nom | La description |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat/)() | Efface le format de tous[`ChartDataLabel`](../chartdatalabel/) dans cette collection. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator/)() | Renvoie un objet énumérateur. |

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

* class [ChartDataLabel](../chartdatalabel/)
* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
