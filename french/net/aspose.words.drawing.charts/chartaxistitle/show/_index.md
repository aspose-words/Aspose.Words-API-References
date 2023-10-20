---
title: ChartAxisTitle.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words pour .NET
description: ChartAxisTitle Show propriété. Détermine si le titre doit être affiché pour laxe. La valeur par défaut estFAUX  en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.charts/chartaxistitle/show/
---
## ChartAxisTitle.Show property

Détermine si le titre doit être affiché pour l'axe. La valeur par défaut est`FAUX` .

```csharp
public bool Show { get; set; }
```

## Exemples

Montre comment définir le titre de l’axe du graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Supprime la série générée par défaut.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

// Définir le titre de l'axe.
chart.AxisX.Title.Text = "Categories";
chart.AxisX.Title.Show = true;
chart.AxisY.Title.Text = "Values";
chart.AxisY.Title.Show = true;
chart.AxisY.Title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Voir également

* class [ChartAxisTitle](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
