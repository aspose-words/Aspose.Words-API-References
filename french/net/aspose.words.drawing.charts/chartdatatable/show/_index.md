---
title: ChartDataTable.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words pour .NET
description: Contrôlez la visibilité de votre graphique avec la propriété « ChartDataTable Show ». Activez/désactivez facilement l'affichage du tableau de données pour une meilleure compréhension des données. Valeur par défaut  false.
type: docs
weight: 70
url: /fr/net/aspose.words.drawing.charts/chartdatatable/show/
---
## ChartDataTable.Show property

Obtient ou définit un indicateur indiquant si la table de données sera affichée pour le graphique. La valeur par défaut est`FAUX` .

```csharp
public bool Show { get; set; }
```

## Remarques

Les types de graphiques suivants ne prennent pas en charge les tableaux de données : Nuage de points, Secteurs, Anneaux, Surface, Radar, Treemap, Sunburst, Histogramme, Pareto, Boîte à moustaches, Cascade, Entonnoir, Graphiques combinés qui incluent des séries de ces types. L'affichage d'un tableau de données pour ces types de graphiques génère unInvalidOperationException exception.

## Exemples

Montre comment afficher un tableau de données avec des données de séries de graphiques.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

ChartSeriesCollection series = chart.Series;
series.Clear();
double[] xValues = new double[] { 2020, 2021, 2022, 2023 };
series.Add("Series1", xValues, new double[] { 5, 11, 2, 7 });
series.Add("Series2", xValues, new double[] { 6, 5.5, 7, 7.8 });
series.Add("Series3", xValues, new double[] { 10, 8, 7, 9 });

ChartDataTable dataTable = chart.DataTable;
dataTable.Show = true;

dataTable.HasLegendKeys = false;
dataTable.HasHorizontalBorder = false;
dataTable.HasVerticalBorder = false;
dataTable.HasOutlineBorder = false;

dataTable.Font.Italic = true;
dataTable.Format.Stroke.Weight = 1;
dataTable.Format.Stroke.DashStyle = DashStyle.ShortDot;
dataTable.Format.Stroke.Color = Color.DarkBlue;

doc.Save(ArtifactsDir + "Charts.DataTable.docx");
```

### Voir également

* class [ChartDataTable](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
