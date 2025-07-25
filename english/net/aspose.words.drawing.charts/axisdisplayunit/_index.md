---
title: AxisDisplayUnit Class
linktitle: AxisDisplayUnit
articleTitle: AxisDisplayUnit
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Drawing.Charts.AxisDisplayUnit class to customize value axis scaling options for enhanced chart clarity and precision.
type: docs
weight: 780
url: /net/aspose.words.drawing.charts/axisdisplayunit/
---
## AxisDisplayUnit class

Provides access to the scaling options of the display units for the value axis.

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/net/working-with-charts/) documentation article.

```csharp
public class AxisDisplayUnit
```

## Constructors

| Name | Description |
| --- | --- |
| [AxisDisplayUnit](axisdisplayunit/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [CustomUnit](../../aspose.words.drawing.charts/axisdisplayunit/customunit/) { get; set; } | Gets or sets a user-defined divisor to scale display units on the value axis. |
| [Document](../../aspose.words.drawing.charts/axisdisplayunit/document/) { get; } | Returns the document containing the parent chart. |
| [Unit](../../aspose.words.drawing.charts/axisdisplayunit/unit/) { get; set; } | Gets or sets the scaling value of the display units as one of the predefined values. |

## Examples

Shows how to manipulate the tick marks and displayed values of a chart axis.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.That(chart.Series.Count, Is.EqualTo(1));
Assert.That(chart.Series[0].Name, Is.EqualTo("Y-Values"));

// Set the minor tick marks of the Y-axis to point away from the plot area,
// and the major tick marks to cross the axis.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Set the Y-axis bounds to -10 and 20.
// This Y-axis will now display 4 major tick marks and 27 minor tick marks.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// For the X-axis, set the major tick marks at every 10 units,
// every minor tick mark at 2.5 units.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Configure both types of tick marks to appear inside the graph plot area.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabels.Alignment = ParagraphAlignment.Right;

Assert.That(axis.TickLabels.Spacing, Is.EqualTo(1));
Assert.That(axis.DisplayUnit.Document, Is.EqualTo(doc));

// Set the tick labels to display their value in millions.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// We can set a more specific value by which tick labels will display their values.
// This statement is equivalent to the one above.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
