---
title: ChartDataTable.HasLegendKeys
linktitle: HasLegendKeys
articleTitle: HasLegendKeys
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartDataTable HasLegendKeys pour contrôler facilement la visibilité des clés de légende dans votre tableau de données. Améliorez la clarté grâce à des paramètres personnalisables !
type: docs
weight: 40
url: /fr/net/aspose.words.drawing.charts/chartdatatable/haslegendkeys/
---
## ChartDataTable.HasLegendKeys property

Obtient ou définit un indicateur indiquant si les clés de légende sont affichées dans la table de données. La valeur par défaut est`vrai` .

```csharp
public bool HasLegendKeys { get; set; }
```

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
