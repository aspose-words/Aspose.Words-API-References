---
title: ChartAxis.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words for .NET
description: ChartAxis Hidden property. Gets or sets a flag indicating whether this axis is hidden or not in C#.
type: docs
weight: 110
url: /net/aspose.words.drawing.charts/chartaxis/hidden/
---
## ChartAxis.Hidden property

Gets or sets a flag indicating whether this axis is hidden or not.

```csharp
public bool Hidden { get; set; }
```

## Remarks

Default value is `false`.

## Examples

Shows how to hide chart axes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Clear the chart's demo data series to start with a clean chart.
chart.Series.Clear();

// Add a custom series with categories for the X-axis, and respective decimal values for the Y-axis.
chart.Series.Add("AW Series 1",
    new[] { "Item 1", "Item 2", "Item 3", "Item 4", "Item 5" },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2 });

// Hide the chart axes to simplify the appearance of the chart. 
chart.AxisX.Hidden = true;
chart.AxisY.Hidden = true;

doc.Save(ArtifactsDir + "Charts.HideChartAxis.docx");
```

### See Also

* class [ChartAxis](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
