---
title: AxisCategoryType Enum
linktitle: AxisCategoryType
articleTitle: AxisCategoryType
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.AxisCategoryType enum. Specifies type of a category axis in C#.
type: docs
weight: 630
url: /net/aspose.words.drawing.charts/axiscategorytype/
---
## AxisCategoryType enumeration

Specifies type of a category axis.

```csharp
public enum AxisCategoryType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Automatic | `0` | Specifies that type of a category axis is determined automatically based on data. |
| Category | `1` | Specifies an axis of an arbitrary set of categories. |
| Time | `2` | Specifies a time category axis. |

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
