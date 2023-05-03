---
title: ChartAxis.NumberFormat
linktitle: NumberFormat
second_title: Aspose.Words for .NET API Reference
description: ChartAxis NumberFormat property. Returns a ChartNumberFormat object that allows defining number formats for the axis in C#.
type: docs
weight: 190
url: /net/aspose.words.drawing.charts/chartaxis/numberformat/
---
## ChartAxis.NumberFormat property

Returns a [`ChartNumberFormat`](../../chartnumberformat/) object that allows defining number formats for the axis.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

## Examples

Shows how to set formatting for chart values.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Clear the chart's demo data series to start with a clean chart.
chart.Series.Clear();

// Add a custom series to the chart with categories for the X-axis,
// and large respective numeric values for the Y-axis. 
chart.Series.Add("Aspose Test Series",
    new [] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

// Set the number format of the Y-axis tick labels to not group digits with commas. 
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// This flag can override the above value and draw the number format from the source cell.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

### See Also

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartAxis](../)
* namespace [Aspose.Words.Drawing.Charts](../../chartaxis/)
* assembly [Aspose.Words](../../../)
