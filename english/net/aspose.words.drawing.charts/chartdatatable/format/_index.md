---
title: ChartDataTable.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words for .NET
description: Discover the ChartDataTable Format property for enhanced text background and border styling, elevating your data visualization experience.
type: docs
weight: 20
url: /net/aspose.words.drawing.charts/chartdatatable/format/
---
## ChartDataTable.Format property

Provides access to fill of text background and border formatting of the data table.

```csharp
public ChartFormat Format { get; }
```

## Examples

Shows how to show data table with chart series data.

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

### See Also

* class [ChartFormat](../../chartformat/)
* class [ChartDataTable](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
