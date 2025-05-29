---
title: Chart.DataTable
linktitle: DataTable
articleTitle: DataTable
second_title: Aspose.Words pour .NET
description: Accédez aux propriétés DataTable de votre graphique et personnalisez-les facilement. Améliorez la visualisation des données avec la propriété Afficher pour des informations claires.
type: docs
weight: 50
url: /fr/net/aspose.words.drawing.charts/chart/datatable/
---
## Chart.DataTable property

Donne accès aux propriétés d'un tableau de données de ce graphique. Le tableau de données peut être affiché à l'aide de[`Show`](../../chartdatatable/show/) propriété.

```csharp
public ChartDataTable DataTable { get; }
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

* class [ChartDataTable](../../chartdatatable/)
* class [Chart](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
