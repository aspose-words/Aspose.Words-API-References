---
title: ChartSeriesGroup.FirstSliceAngle
linktitle: FirstSliceAngle
articleTitle: FirstSliceAngle
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartSeriesGroup FirstSliceAngle pour personnaliser l'angle de la première tranche de votre graphique à secteurs en degrés pour une visualisation améliorée des données.
type: docs
weight: 60
url: /fr/net/aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/
---
## ChartSeriesGroup.FirstSliceAngle property

Obtient ou définit l'angle, en degrés, de la première tranche du graphique à secteurs parent.

```csharp
public int FirstSliceAngle { get; set; }
```

## Remarques

S'applique aux groupes de séries duPie ,Pie3D etDoughnut types.

La plage de valeurs acceptables s'étend de 0 à 360 inclus. La valeur par défaut est 0.

## Exemples

Montre comment créer et formater un graphique en anneau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Doughnut, 400, 400);
Chart chart = shape.Chart;
// Supprimez la série générée par défaut.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
chart.Series.Add("Series 1", categories, new double[] { 4, 2, 5 });

// Formater le graphique en anneau.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.DoughnutHoleSize = 10;
seriesGroup.FirstSliceAngle = 270;

doc.Save(ArtifactsDir + "Charts.DoughnutChart.docx");
```

### Voir également

* class [ChartSeriesGroup](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
