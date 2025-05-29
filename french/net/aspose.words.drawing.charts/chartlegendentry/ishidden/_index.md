---
title: ChartLegendEntry.IsHidden
linktitle: IsHidden
articleTitle: IsHidden
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartLegendEntry IsHidden pour contrôler facilement la visibilité de la légende de votre graphique. Améliorez la présentation de vos données grâce à cette simple fonctionnalité de basculement !
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.charts/chartlegendentry/ishidden/
---
## ChartLegendEntry.IsHidden property

Obtient ou définit une valeur indiquant si cette entrée est masquée dans la légende du graphique. La valeur par défaut est**FAUX** .

```csharp
public bool IsHidden { get; set; }
```

## Remarques

Lorsqu'une entrée de légende de graphique est masquée, cela n'affecte pas la série de graphiques ou la ligne de tendance correspondante qui est toujours affichée sur le graphique.

## Exemples

Montre comment travailler avec une entrée de légende pour une série de graphiques.

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

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### Voir également

* class [ChartLegendEntry](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
