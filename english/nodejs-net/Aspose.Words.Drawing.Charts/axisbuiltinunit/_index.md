---
title: AxisBuiltInUnit enumeration
linktitle: AxisBuiltInUnit enumeration
articleTitle: AxisBuiltInUnit enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Charts.AxisBuiltInUnit enumeration. Specifies the display units for an axis."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Drawing.Charts/axisbuiltinunit/
---

## AxisBuiltInUnit enumeration

Specifies the display units for an axis.


### Members

| Name | Description |
| --- | --- |
| None | Specifies the values on the chart shall displayed as is. |
| Custom | Specifies the values on the chart shall be divided by a user-defined divisor. This value is not supported by the new chart types of MS Office 2016. |
| Billions | Specifies the values on the chart shall be divided by 1,000,000,000. |
| HundredMillions | Specifies the values on the chart shall be divided by 100,000,000. |
| Hundreds | Specifies the values on the chart shall be divided by 100. |
| HundredThousands | Specifies the values on the chart shall be divided by 100,000. |
| Millions | Specifies the values on the chart shall be divided by 1,000,000. |
| TenMillions | Specifies the values on the chart shall be divided by 10,000,000. |
| TenThousands | Specifies the values on the chart shall be divided by 10,000. |
| Thousands | Specifies the values on the chart shall be divided by 1,000. |
| Trillions | Specifies the values on the chart shall be divided by 1,000,000,000,0000. |
| Percentage | Specifies the values on the chart shall be divided by 0.01. This value is supported only by the new chart types of MS Office 2016. |

### Examples

Shows how to manipulate the tick marks and displayed values of a chart axis.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Scatter, 450, 250);
let chart = shape.chart;

expect(chart.series.count).toEqual(1);
expect(chart.series.at(0).name).toEqual("Y-Values");

// Set the minor tick marks of the Y-axis to point away from the plot area,
// and the major tick marks to cross the axis.
let axis = chart.axisY;
axis.majorTickMark = aw.Drawing.Charts.AxisTickMark.Cross;
axis.minorTickMark = aw.Drawing.Charts.AxisTickMark.Outside;

// Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
axis.majorUnit = 10;
axis.minorUnit = 1;

// Set the Y-axis bounds to -10 and 20.
// This Y-axis will now display 4 major tick marks and 27 minor tick marks.
axis.scaling.minimum = new aw.Drawing.Charts.AxisBound(-10);
axis.scaling.maximum = new aw.Drawing.Charts.AxisBound(20);

// For the X-axis, set the major tick marks at every 10 units,
// every minor tick mark at 2.5 units.
axis = chart.axisX;
axis.majorUnit = 10;
axis.minorUnit = 2.5;

// Configure both types of tick marks to appear inside the graph plot area.
axis.majorTickMark = aw.Drawing.Charts.AxisTickMark.Inside;
axis.minorTickMark = aw.Drawing.Charts.AxisTickMark.Inside;

// Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
axis.scaling.minimum = new aw.Drawing.Charts.AxisBound(-10);
axis.scaling.maximum = new aw.Drawing.Charts.AxisBound(30);
axis.tickLabels.alignment = aw.ParagraphAlignment.Right;

expect(axis.tickLabels.spacing).toEqual(1);

// Set the tick labels to display their value in millions.
axis.displayUnit.unit = aw.Drawing.Charts.AxisBuiltInUnit.Millions;

// We can set a more specific value by which tick labels will display their values.
// This statement is equivalent to the one above.
axis.displayUnit.customUnit = 1000000;
expect(axis.displayUnit.unit).toEqual(aw.Drawing.Charts.AxisBuiltInUnit.Custom);

doc.save(base.artifactsDir + "Charts.AxisDisplayUnit.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../)

