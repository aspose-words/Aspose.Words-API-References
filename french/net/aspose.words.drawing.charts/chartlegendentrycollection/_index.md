---
title: Class ChartLegendEntryCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.ChartLegendEntryCollection classe. Représente une collection dentrées de légende de graphique.
type: docs
weight: 740
url: /fr/net/aspose.words.drawing.charts/chartlegendentrycollection/
---
## ChartLegendEntryCollection class

Représente une collection d'entrées de légende de graphique.

Pour en savoir plus, visitez le[Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) article documentaire.

```csharp
public class ChartLegendEntryCollection : IEnumerable<ChartLegendEntry>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartlegendentrycollection/count/) { get; } | Renvoie le nombre de[`ChartLegendEntry`](../chartlegendentry/) dans cette collection. |
| [Item](../../aspose.words.drawing.charts/chartlegendentrycollection/item/) { get; } | Retours[`ChartLegendEntry`](../chartlegendentry/) pour l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartlegendentrycollection/getenumerator/)() | Renvoie un objet énumérateur. |

### Exemples

Montre comment utiliser une entrée de légende pour les séries de graphiques.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "AW Category 1", "AW Category 2" };

ChartSeries series1 = series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });
series.Add("Series 3", categories, new double[] { 5, 6 });
series.Add("Series 4", categories, new double[] { 0, 0 });

ChartLegendEntryCollection legendEntries = chart.Legend.LegendEntries;
legendEntries[3].IsHidden = true;

foreach (ChartLegendEntry legendEntry in legendEntries)
    legendEntry.Font.Size = 12;

series1.LegendEntry.Font.Italic = true;

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### Voir également

* class [ChartLegendEntry](../chartlegendentry/)
* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)


