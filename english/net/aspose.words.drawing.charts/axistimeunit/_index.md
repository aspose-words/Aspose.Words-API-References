---
title: AxisTimeUnit Enum
linktitle: AxisTimeUnit
articleTitle: AxisTimeUnit
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.AxisTimeUnit enum. Specifies the unit of time for axes in C#.
type: docs
weight: 750
url: /net/aspose.words.drawing.charts/axistimeunit/
---
## AxisTimeUnit enumeration

Specifies the unit of time for axes.

```csharp
public enum AxisTimeUnit
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Automatic | `0` | Specifies that unit was not set explicitly and default value should be used. |
| Days | `1` | Specifies that the chart data shall be shown in days. |
| Months | `2` | Specifies that the chart data shall be shown in months. |
| Years | `3` | Specifies that the chart data shall be shown in years. |

## Examples

Shows how to insert chart with date/time values.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Clear the chart's demo data series to start with a clean chart.
chart.Series.Clear();

// Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// Set lower and upper bounds for the X-axis.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// Set the major units of the X-axis to a week, and the minor units to a day.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;
xAxis.HasMajorGridlines = true;
xAxis.HasMinorGridlines = true;

// Define Y-axis properties for decimal values.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabels.Position = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);
yAxis.HasMajorGridlines = true;
yAxis.HasMinorGridlines = true;

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
