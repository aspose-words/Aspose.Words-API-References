---
title: ChartLegend.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Format ChartLegend pour une personnalisation facile du remplissage de la légende et des styles de ligne, améliorant ainsi votre expérience de visualisation des données.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.charts/chartlegend/format/
---
## ChartLegend.Format property

Donne accès au remplissage et au formatage des lignes de la légende.

```csharp
public ChartFormat Format { get; }
```

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

* class [ChartFormat](../../chartformat/)
* class [ChartLegend](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
