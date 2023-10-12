---
title: ChartLegendEntry.Font
second_title: Référence de l'API Aspose.Words pour .NET
description: ChartLegendEntry propriété. Donne accès au formatage de la police de cette entrée de légende.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.charts/chartlegendentry/font/
---
## ChartLegendEntry.Font property

Donne accès au formatage de la police de cette entrée de légende.

```csharp
public Font Font { get; }
```

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

* class [Font](../../../aspose.words/font/)
* class [ChartLegendEntry](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../chartlegendentry/)
* Assemblée [Aspose.Words](../../../)


