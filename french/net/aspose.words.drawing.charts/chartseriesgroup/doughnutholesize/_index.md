---
title: ChartSeriesGroup.DoughnutHoleSize
linktitle: DoughnutHoleSize
articleTitle: DoughnutHoleSize
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartSeriesGroup DoughnutHoleSize pour personnaliser facilement le pourcentage de taille de trou de votre graphique en anneau pour une visualisation améliorée des données.
type: docs
weight: 50
url: /fr/net/aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/
---
## ChartSeriesGroup.DoughnutHoleSize property

Obtient ou définit la taille du trou du graphique en anneau parent sous forme de pourcentage.

```csharp
public int DoughnutHoleSize { get; set; }
```

## Remarques

S'applique uniquement aux groupes de séries duDoughnut taper.

La plage de valeurs acceptables s'étend de 0 à 90 inclus. La valeur par défaut est 75.

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
