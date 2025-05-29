---
title: ChartAxisTitle.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words pour .NET
description: Découvrez la propriété « Afficher » de ChartAxisTitle pour contrôler la visibilité des titres d'axe. Améliorez vos graphiques avec des titres clairs et informatifs pour une meilleure compréhension des données.
type: docs
weight: 40
url: /fr/net/aspose.words.drawing.charts/chartaxistitle/show/
---
## ChartAxisTitle.Show property

Détermine si le titre doit être affiché pour l'axe. La valeur par défaut est`FAUX` .

```csharp
public bool Show { get; set; }
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

* class [ChartAxisTitle](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
