---
title: AxisBuiltInUnit Enum
linktitle: AxisBuiltInUnit
articleTitle: AxisBuiltInUnit
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.AxisBuiltInUnit enum. Specifies the display units for an axis in C#.
type: docs
weight: 600
url: /net/aspose.words.drawing.charts/axisbuiltinunit/
---
## AxisBuiltInUnit enumeration

Specifies the display units for an axis.

```csharp
public enum AxisBuiltInUnit
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | Specifies the values on the chart shall displayed as is. |
| Custom | `1` | Specifies the values on the chart shall be divided by a user-defined divisor. This value is not supported by the new chart types of MS Office 2016. |
| Billions | `2` | Specifies the values on the chart shall be divided by 1,000,000,000. |
| HundredMillions | `3` | Specifies the values on the chart shall be divided by 100,000,000. |
| Hundreds | `4` | Specifies the values on the chart shall be divided by 100. |
| HundredThousands | `5` | Specifies the values on the chart shall be divided by 100,000. |
| Millions | `6` | Specifies the values on the chart shall be divided by 1,000,000. |
| TenMillions | `7` | Specifies the values on the chart shall be divided by 10,000,000. |
| TenThousands | `8` | Specifies the values on the chart shall be divided by 10,000. |
| Thousands | `9` | Specifies the values on the chart shall be divided by 1,000. |
| Trillions | `10` | Specifies the values on the chart shall be divided by 1,000,000,000,0000. |
| Percentage | `11` | Specifies the values on the chart shall be divided by 0.01. This value is supported only by the new chart types of MS Office 2016. |

## Examples

Shows how to manipulate the tick marks and displayed values of a chart axis.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

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
axis.TickLabelAlignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabelSpacing);

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
