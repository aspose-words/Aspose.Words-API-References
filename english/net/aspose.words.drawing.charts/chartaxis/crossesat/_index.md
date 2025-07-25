---
title: ChartAxis.CrossesAt
linktitle: CrossesAt
articleTitle: CrossesAt
second_title: Aspose.Words for .NET
description: Discover the ChartAxis CrossesAt property to easily define intersection points on your chart's perpendicular axis for enhanced data visualization.
type: docs
weight: 50
url: /net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

Specifies where on the perpendicular axis the axis crosses.

```csharp
public double CrossesAt { get; set; }
```

## Remarks

The property has effect only if [`Crosses`](../crosses/) are set to Custom. It is not supported by MS Office 2016 new charts.

The units are determined by the type of axis. When the axis is a value axis, the value of the property is a decimal number on the value axis. When the axis is a time category axis, the value is defined as an integer number of days relative to the base date (30/12/1899). For a text category axis, the value is an integer category number, starting with 1 as the first category.

## Examples

Shows how to get a graph axis to cross at a custom location.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.That(chart.Series.Count, Is.EqualTo(3));
Assert.That(chart.Series[0].Name, Is.EqualTo("Series 1"));
Assert.That(chart.Series[1].Name, Is.EqualTo("Series 2"));
Assert.That(chart.Series[2].Name, Is.EqualTo("Series 3"));

// For column charts, the Y-axis crosses at zero by default,
// which means that columns for all values below zero point down to represent negative values.
// We can set a different value for the Y-axis crossing. In this case, we will set it to 3.
ChartAxis axis = chart.AxisX;
axis.Crosses = AxisCrosses.Custom;
axis.CrossesAt = 3;
axis.AxisBetweenCategories = true;

doc.Save(ArtifactsDir + "Charts.AxisCross.docx");
```

### See Also

* class [ChartAxis](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
