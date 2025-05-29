---
title: ChartFormat Class
linktitle: ChartFormat
articleTitle: ChartFormat
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.ChartFormat pour un style avancé des éléments de graphique. Améliorez vos documents avec des graphiques professionnels et personnalisables.
type: docs
weight: 1000
url: /fr/net/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class

Représente la mise en forme d'un élément de graphique.

Pour en savoir plus, visitez le[Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) article de documentation.

```csharp
public class ChartFormat
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Fill](../../aspose.words.drawing.charts/chartformat/fill/) { get; } | Obtient la mise en forme de remplissage pour l'élément de graphique parent. |
| [IsDefined](../../aspose.words.drawing.charts/chartformat/isdefined/) { get; } | Obtient un indicateur indiquant si un format est défini. |
| [ShapeType](../../aspose.words.drawing.charts/chartformat/shapetype/) { get; set; } | Obtient ou définit le type de forme de l'élément de graphique parent. |
| [Stroke](../../aspose.words.drawing.charts/chartformat/stroke/) { get; } | Obtient la mise en forme de ligne pour l'élément de graphique parent. |

## Méthodes

| Nom | La description |
| --- | --- |
| [SetDefaultFill](../../aspose.words.drawing.charts/chartformat/setdefaultfill/)() | Réinitialise le remplissage de l'élément de graphique pour avoir la valeur par défaut. |

## Exemples

Montre comment utiliser le formatage des graphiques.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Supprimer les séries générées par défaut.
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// Formater l'arrière-plan du graphique.
chart.Format.Fill.Solid(Color.DarkSlateGray);

// Masquer les étiquettes des graduations des axes.
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// Formater le titre du graphique.
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Formater le titre de l'axe.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Formater la légende.
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
