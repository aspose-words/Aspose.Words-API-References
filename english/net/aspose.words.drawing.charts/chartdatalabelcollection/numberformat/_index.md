---
title: ChartDataLabelCollection.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words for .NET
description: ChartDataLabelCollection NumberFormat property. Gets an ChartNumberFormat instance allowing to set number format for the data labels of the entire series in C#.
type: docs
weight: 50
url: /net/aspose.words.drawing.charts/chartdatalabelcollection/numberformat/
---
## ChartDataLabelCollection.NumberFormat property

Gets an [`ChartNumberFormat`](../../chartnumberformat/) instance allowing to set number format for the data labels of the entire series.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

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

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartDataLabelCollection](../)
* namespace [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection/)
* assembly [Aspose.Words](../../../)
