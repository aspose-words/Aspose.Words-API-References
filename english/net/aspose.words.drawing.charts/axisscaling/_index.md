---
title: AxisScaling Class
linktitle: AxisScaling
articleTitle: AxisScaling
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.AxisScaling class. Represents the scaling options of the axis in C#.
type: docs
weight: 570
url: /net/aspose.words.drawing.charts/axisscaling/
---
## AxisScaling class

Represents the scaling options of the axis.

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/net/working-with-charts/) documentation article.

```csharp
public class AxisScaling
```

## Constructors

| Name | Description |
| --- | --- |
| [AxisScaling](axisscaling/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [LogBase](../../aspose.words.drawing.charts/axisscaling/logbase/) { get; set; } | Gets or sets the logarithmic base for a logarithmic axis. |
| [Maximum](../../aspose.words.drawing.charts/axisscaling/maximum/) { get; set; } | Gets or sets the maximum value of the axis. |
| [Minimum](../../aspose.words.drawing.charts/axisscaling/minimum/) { get; set; } | Gets or sets minimum value of the axis. |
| [Type](../../aspose.words.drawing.charts/axisscaling/type/) { get; set; } | Gets or sets scaling type of the axis. |

## Examples

Shows how to apply logarithmic scaling to a chart axis.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Clear the chart's demo data series to start with a clean chart.
chart.Series.Clear();

// Insert a series with X/Y coordinates for five points.
chart.Series.Add("Series 1",
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 },
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// The scaling of the X-axis is linear by default,
// displaying evenly incrementing values that cover our X-value range (0, 1, 2, 3...).
// A linear axis is not ideal for our Y-values
// since the points with the smaller Y-values will be harder to read.
// A logarithmic scaling with a base of 20 (1, 20, 400, 8000...)
// will spread the plotted points, allowing us to read their values on the chart more easily.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
