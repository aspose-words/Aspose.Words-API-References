---
title: ChartDataTable.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words pour .NET
description: Découvrez la propriété de police ChartDataTable pour améliorer l'apparence de votre tableau de données avec un formatage de police personnalisable pour une meilleure lisibilité et un meilleur impact.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.charts/chartdatatable/font/
---
## ChartDataTable.Font property

Donne accès au formatage des polices du tableau de données.

```csharp
public Font Font { get; }
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

* class [Font](../../../aspose.words/font/)
* class [ChartDataTable](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
