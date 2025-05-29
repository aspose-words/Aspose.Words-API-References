---
title: ChartSeriesGroup.SecondSectionSize
linktitle: SecondSectionSize
articleTitle: SecondSectionSize
second_title: Aspose.Words pour .NET
description: Découvrez comment ajuster la propriété SecondSectionSize dans ChartSeriesGroup pour personnaliser efficacement la taille de la section secondaire de votre graphique à secteurs.
type: docs
weight: 90
url: /fr/net/aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/
---
## ChartSeriesGroup.SecondSectionSize property

Obtient ou définit la taille de la section secondaire du graphique à secteurs sous forme de pourcentage.

```csharp
public int SecondSectionSize { get; set; }
```

## Remarques

S'applique aux groupes de séries duPieOfPie et PieOfBar types.

La plage de valeurs acceptables s'étend de 5 à 200 inclus. La valeur par défaut est 75.

## Exemples

Montre comment créer et formater un graphique à secteurs.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.PieOfPie, 440, 300);
Chart chart = shape.Chart;
// Supprimez la série générée par défaut.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3", "Category 4" };
chart.Series.Add("Series 1", categories, new double[] { 11, 8, 4, 3 });

// Formater le graphique à secteurs.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.GapWidth = 10;
seriesGroup.SecondSectionSize = 77;

doc.Save(ArtifactsDir + "Charts.PieOfPieChart.docx");
```

### Voir également

* class [ChartSeriesGroup](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
