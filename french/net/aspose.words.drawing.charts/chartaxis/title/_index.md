---
title: ChartAxis.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartAxis Title pour un accès et une personnalisation faciles des titres des axes, améliorant ainsi la visualisation et la présentation de vos données.
type: docs
weight: 250
url: /fr/net/aspose.words.drawing.charts/chartaxis/title/
---
## ChartAxis.Title property

Donne accès aux propriétés du titre de l'axe.

```csharp
public ChartAxisTitle Title { get; }
```

## Exemples

Montre comment définir le titre de l'axe du graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Supprimer la série générée par défaut.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

ChartAxisTitle chartAxisXTitle = chart.AxisX.Title;
chartAxisXTitle.Text = "Categories";
chartAxisXTitle.Show = true;
ChartAxisTitle chartAxisYTitle = chart.AxisY.Title;
chartAxisYTitle.Text = "Values";
chartAxisYTitle.Show = true;
chartAxisYTitle.Overlay = true;
chartAxisYTitle.Font.Size = 12;
chartAxisYTitle.Font.Color = Color.Blue;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Voir également

* class [ChartAxisTitle](../../chartaxistitle/)
* class [ChartAxis](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
