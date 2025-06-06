---
title: ChartDataLabelCollection.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words for .NET
description: Access and customize the font formatting of your entire series' data labels with the ChartDataLabelCollection Font property for enhanced data visualization.
type: docs
weight: 20
url: /net/aspose.words.drawing.charts/chartdatalabelcollection/font/
---
## ChartDataLabelCollection.Font property

Provides access to the font formatting of the data labels of the entire series.

```csharp
public Font Font { get; }
```

## Remarks

Value defined for this property can be overridden for an individual data label with using the [`Font`](../../chartdatalabel/font/) property.

## Examples

Shows how to enable and configure data labels for a chart series.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Add a line chart, then clear its demo data series to start with a clean chart,
// and then set a title.
Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;
chart.Series.Clear();
chart.Title.Text = "Monthly sales report";

// Insert a custom chart series with months as categories for the X-axis,
// and respective decimal amounts for the Y-axis.
ChartSeries series = chart.Series.Add("Revenue",
    new[] { "January", "February", "March" },
    new[] { 25.611d, 21.439d, 33.750d });

// Enable data labels, and then apply a custom number format for values displayed in the data labels.
// This format will treat displayed decimal values as millions of US Dollars.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.NumberFormat.FormatCode = "\"US$\" #,##0.000\"M\"";
dataLabels.Font.Size = 12;

doc.Save(ArtifactsDir + "Charts.DataLabelNumberFormat.docx");
```

### See Also

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabelCollection](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
