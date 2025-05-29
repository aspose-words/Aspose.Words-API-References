---
title: ChartDataTable.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words för .NET
description: Styr ditt diagrams synlighet med egenskapen ChartDataTable Show. Växla enkelt mellan visning av datatabeller för förbättrad datainsikt. Standardinställningen är falsk.
type: docs
weight: 70
url: /sv/net/aspose.words.drawing.charts/chartdatatable/show/
---
## ChartDataTable.Show property

Hämtar eller ställer in en flagga som anger om datatabellen ska visas för diagrammet. Standardvärdet är`falsk` .

```csharp
public bool Show { get; set; }
```

## Anmärkningar

Följande diagramtyper stöder inte datatabeller: Scatter-, Pie-, Doughnut-, Surface-, Radar-, Treemap-, Sunburst-, Histogram-, Pareto-, Box and Whisker-, Waterfall-, Funnel- och Combo-diagram som innehåller serier av dessa typer. Att visa en datatabell för diagramtyperna ger enInvalidOperationException undantag.

## Exempel

Visar hur man visar datatabeller med diagramseriedata.

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

### Se även

* class [ChartDataTable](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
