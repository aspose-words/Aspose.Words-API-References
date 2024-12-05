---
title: ChartNumberFormat Class
linktitle: ChartNumberFormat
articleTitle: ChartNumberFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartNumberFormat class. Represents number formatting of the parent element in C#.
type: docs
weight: 1040
url: /net/aspose.words.drawing.charts/chartnumberformat/
---
## ChartNumberFormat class

Represents number formatting of the parent element.

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/net/working-with-charts/) documentation article.

```csharp
public class ChartNumberFormat
```

## Properties

| Name | Description |
| --- | --- |
| [FormatCode](../../aspose.words.drawing.charts/chartnumberformat/formatcode/) { get; set; } | Gets or sets the format code applied to a data label. |
| [IsLinkedToSource](../../aspose.words.drawing.charts/chartnumberformat/islinkedtosource/) { get; set; } | Specifies whether the format code is linked to a source cell. Default is true. |

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
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

// Set the number format of the Y-axis tick labels to not group digits with commas. 
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// This flag can override the above value and draw the number format from the source cell.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
