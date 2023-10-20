---
title: ChartAxisTitle Class
linktitle: ChartAxisTitle
articleTitle: ChartAxisTitle
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.ChartAxisTitle classe. Donne accès aux propriétés du titre de laxe en C#.
type: docs
weight: 650
url: /fr/net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

Donne accès aux propriétés du titre de l'axe.

Pour en savoir plus, visitez le[Travailler avec des graphiques ](https://docs.aspose.com/words/net/working-with-charts/) article documentaire.

```csharp
public class ChartAxisTitle
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | Détermine si d'autres éléments du graphique doivent pouvoir chevaucher le titre. La valeur par défaut est`FAUX` . |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | Détermine si le titre doit être affiché pour l'axe. La valeur par défaut est`FAUX` . |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | Obtient ou définit le texte du titre de l'axe. Si`nul` ou une valeur vide est spécifiée, le titre généré automatiquement sera affiché. |

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

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
