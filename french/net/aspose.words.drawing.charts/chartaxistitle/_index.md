---
title: ChartAxisTitle Class
linktitle: ChartAxisTitle
articleTitle: ChartAxisTitle
second_title: Aspose.Words pour .NET
description: Explorez la classe Aspose.Words.ChartAxisTitle pour gérer facilement les propriétés du titre de l'axe et améliorer l'impact visuel de votre document.
type: docs
weight: 910
url: /fr/net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

Donne accès aux propriétés du titre de l'axe.

Pour en savoir plus, visitez le[Travailler avec des graphiques x000d](https://docs.aspose.com/words/net/working-with-charts/) article de documentation.

```csharp
public class ChartAxisTitle
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartaxistitle/font/) { get; } | Donne accès à la mise en forme de la police du titre de l'axe. |
| [Format](../../aspose.words.drawing.charts/chartaxistitle/format/) { get; } | Donne accès au remplissage et au formatage des lignes du titre de l'axe. |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | Détermine si d'autres éléments du graphique doivent être autorisés à chevaucher le titre. La valeur par défaut est`FAUX` . |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | Détermine si le titre doit être affiché pour l'axe. La valeur par défaut est`FAUX` . |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | Obtient ou définit le texte du titre de l'axe. Si`nul` ou une valeur vide est spécifiée, le titre généré automatiquement sera affiché. |

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

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
