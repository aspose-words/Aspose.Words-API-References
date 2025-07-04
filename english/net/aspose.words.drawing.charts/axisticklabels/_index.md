---
title: AxisTickLabels Class
linktitle: AxisTickLabels
articleTitle: AxisTickLabels
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Drawing.Charts.AxisTickLabels class, designed to enhance your chart's axis tick mark labels with customizable properties for better data visualization.
type: docs
weight: 830
url: /net/aspose.words.drawing.charts/axisticklabels/
---
## AxisTickLabels class

Represents properties of axis tick mark labels.

```csharp
public class AxisTickLabels
```

## Properties

| Name | Description |
| --- | --- |
| [Alignment](../../aspose.words.drawing.charts/axisticklabels/alignment/) { get; set; } | Gets or sets text alignment of the axis tick labels. |
| [Font](../../aspose.words.drawing.charts/axisticklabels/font/) { get; } | Provides access to font formatting of the tick labels. |
| [IsAutoSpacing](../../aspose.words.drawing.charts/axisticklabels/isautospacing/) { get; set; } | Gets or sets a flag indicating whether to use automatic interval for drawing the tick labels. |
| [Offset](../../aspose.words.drawing.charts/axisticklabels/offset/) { get; set; } | Gets or sets the distance of the tick labels from the axis. |
| [Orientation](../../aspose.words.drawing.charts/axisticklabels/orientation/) { get; set; } | Gets or sets the orientation of the tick label text. |
| [Position](../../aspose.words.drawing.charts/axisticklabels/position/) { get; set; } | Gets or sets the position of the tick labels on the axis. |
| [Rotation](../../aspose.words.drawing.charts/axisticklabels/rotation/) { get; set; } | Gets or sets the rotation of the tick labels in degrees. |
| [Spacing](../../aspose.words.drawing.charts/axisticklabels/spacing/) { get; set; } | Gets or sets the interval at which the tick labels are drawn. |

## Examples

Shows how to insert a chart and modify the appearance of its axes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Clear the chart's demo data series to start with a clean chart.
chart.Series.Clear();

// Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Chart axes have various options that can change their appearance,
// such as their direction, major/minor unit ticks, and tick marks.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabels.Offset = 50;
xAxis.TickLabels.Position = AxisTickLabelPosition.Low;
xAxis.TickLabels.IsAutoSpacing = false;
xAxis.TickMarkSpacing = 1;

Assert.That(xAxis.Document, Is.EqualTo(doc));

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabels.Position = AxisTickLabelPosition.NextToAxis;
yAxis.TickLabels.Alignment = ParagraphAlignment.Center;
yAxis.TickLabels.Font.Color = Color.Red;
yAxis.TickLabels.Spacing = 1;

// Column charts do not have a Z-axis.
Assert.That(chart.AxisZ, Is.Null);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
