---
title: ChartDataTable Class
linktitle: ChartDataTable
articleTitle: ChartDataTable
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Drawing.Charts.ChartDataTable class to easily customize chart data tables and enhance your data visualization with powerful features.
type: docs
weight: 980
url: /net/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class

Allows to specify properties of a chart data table.

```csharp
public class ChartDataTable
```

## Properties

| Name | Description |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatatable/font/) { get; } | Provides access to font formatting of the data table. |
| [Format](../../aspose.words.drawing.charts/chartdatatable/format/) { get; } | Provides access to fill of text background and border formatting of the data table. |
| [HasHorizontalBorder](../../aspose.words.drawing.charts/chartdatatable/hashorizontalborder/) { get; set; } | Gets or sets a flag indicating whether a horizontal border of the data table is displayed. The default value is `true`. |
| [HasLegendKeys](../../aspose.words.drawing.charts/chartdatatable/haslegendkeys/) { get; set; } | Gets or sets a flag indicating whether legend keys are displayed in the data table. The default value is `true`. |
| [HasOutlineBorder](../../aspose.words.drawing.charts/chartdatatable/hasoutlineborder/) { get; set; } | Gets or sets a flag indicating whether an outline border, that is, a border around series and category names, is displayed. The default value is `true`. |
| [HasVerticalBorder](../../aspose.words.drawing.charts/chartdatatable/hasverticalborder/) { get; set; } | Gets or sets a flag indicating whether a vertical border of the data table is displayed. The default value is `true`. |
| [Show](../../aspose.words.drawing.charts/chartdatatable/show/) { get; set; } | Gets or sets a flag indicating whether the data table will be shown for the chart. Default value is `false`. |

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

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
