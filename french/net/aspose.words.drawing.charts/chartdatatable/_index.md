---
title: ChartDataTable Class
linktitle: ChartDataTable
articleTitle: ChartDataTable
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.Charts.ChartDataTable pour personnaliser facilement les tableaux de données des graphiques et améliorer votre visualisation de données avec des fonctionnalités puissantes.
type: docs
weight: 990
url: /fr/net/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class

Permet de spécifier les propriétés d'une table de données de graphique.

```csharp
public class ChartDataTable
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatatable/font/) { get; } | Donne accès au formatage des polices du tableau de données. |
| [Format](../../aspose.words.drawing.charts/chartdatatable/format/) { get; } | Donne accès au remplissage de l'arrière-plan du texte et au formatage des bordures du tableau de données. |
| [HasHorizontalBorder](../../aspose.words.drawing.charts/chartdatatable/hashorizontalborder/) { get; set; } | Obtient ou définit un indicateur indiquant si une bordure horizontale du tableau de données est affichée. La valeur par défaut est`vrai` . |
| [HasLegendKeys](../../aspose.words.drawing.charts/chartdatatable/haslegendkeys/) { get; set; } | Obtient ou définit un indicateur indiquant si les clés de légende sont affichées dans la table de données. La valeur par défaut est`vrai` . |
| [HasOutlineBorder](../../aspose.words.drawing.charts/chartdatatable/hasoutlineborder/) { get; set; } | Obtient ou définit un indicateur indiquant si une bordure de contour, c'est-à-dire une bordure autour des noms de séries et de catégories, est affichée. La valeur par défaut est`vrai` . |
| [HasVerticalBorder](../../aspose.words.drawing.charts/chartdatatable/hasverticalborder/) { get; set; } | Obtient ou définit un indicateur indiquant si une bordure verticale du tableau de données est affichée. La valeur par défaut est`vrai` . |
| [Show](../../aspose.words.drawing.charts/chartdatatable/show/) { get; set; } | Obtient ou définit un indicateur indiquant si la table de données sera affichée pour le graphique. La valeur par défaut est`FAUX` . |

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

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
