---
title: AxisCrosses Enum
linktitle: AxisCrosses
articleTitle: AxisCrosses
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.AxisCrosses enum. Specifies the possible crossing points for an axis in C#.
type: docs
weight: 640
url: /net/aspose.words.drawing.charts/axiscrosses/
---
## AxisCrosses enumeration

Specifies the possible crossing points for an axis.

```csharp
public enum AxisCrosses
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Automatic | `0` | The category axis crosses at the zero point of the value axis (if possible), or at the minimum value if the minimum is greater than zero, or at the maximum if the maximum is less than zero. |
| Maximum | `1` | A perpendicular axis crosses at the maximum value of the axis. |
| Minimum | `2` | A perpendicular axis crosses at the minimum value of the axis. |
| Custom | `3` | A perpendicular axis crosses at the specified value of the axis. |

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

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabels.Position = AxisTickLabelPosition.NextToAxis;

// Column charts do not have a Z-axis.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
