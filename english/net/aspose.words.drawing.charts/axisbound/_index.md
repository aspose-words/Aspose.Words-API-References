---
title: AxisBound Class
linktitle: AxisBound
articleTitle: AxisBound
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Drawing.Charts.AxisBound class, your solution for defining axis value limits in charts for precise data visualization.
type: docs
weight: 740
url: /net/aspose.words.drawing.charts/axisbound/
---
## AxisBound class

Represents minimum or maximum bound of axis values.

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/net/working-with-charts/) documentation article.

```csharp
public sealed class AxisBound
```

## Constructors

| Name | Description |
| --- | --- |
| [AxisBound](axisbound/#constructor)() | Creates a new instance indicating that axis bound should be determined automatically by a word-processing application. |
| [AxisBound](axisbound/#constructor_2)(*DateTime*) | Creates an axis bound represented as datetime value. |
| [AxisBound](axisbound/#constructor_1)(*double*) | Creates an axis bound represented as a number. |

## Properties

| Name | Description |
| --- | --- |
| [IsAuto](../../aspose.words.drawing.charts/axisbound/isauto/) { get; } | Returns a flag indicating that axis bound should be determined automatically. |
| [Value](../../aspose.words.drawing.charts/axisbound/value/) { get; } | Returns numeric value of axis bound. |
| [ValueAsDate](../../aspose.words.drawing.charts/axisbound/valueasdate/) { get; } | Returns value of axis bound represented as datetime. |

## Methods

| Name | Description |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/axisbound/equals/)(*object*) | Determines whether the specified object is equal in value to the current object. |
| override [GetHashCode](../../aspose.words.drawing.charts/axisbound/gethashcode/)() | Serves as a hash function for this type. |
| override [ToString](../../aspose.words.drawing.charts/axisbound/tostring/)() | Returns a user-friendly string that displays the value of this object. |

## Remarks

Bound can be specified as a numeric, datetime or a special "auto" value.

The instances of this class are immutable.

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
