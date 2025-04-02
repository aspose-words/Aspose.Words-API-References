---
title: AxisScaling.minimum property
linktitle: minimum property
articleTitle: minimum property
second_title: Aspose.Words for NodeJs
description: "AxisScaling.minimum property. Gets or sets minimum value of the axis."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Drawing.Charts/axisscaling/minimum/
---

## AxisScaling.minimum property

Gets or sets minimum value of the axis.


```js
get minimum(): Aspose.Words.Drawing.Charts.AxisBound
```

### Remarks

The default value is "auto".


### Examples

Shows how to insert chart with date/time values.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Line, 500, 300);
let chart = shape.chart;

// Clear the chart's demo data series to start with a clean chart.
chart.series.clear();

// Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
chart.series.add("Aspose Test Series",
  [
    Date.parse("2017-11-06"), Date.parse("2017-11-09"), Date.parse("2017-11-15"),
    Date.parse("2017-11-21"), Date.parse("2017-11-25"), Date.parse("2017-11-29")
  ],
  [ 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 ]);


// Set lower and upper bounds for the X-axis.
let xAxis = chart.axisX;
xAxis.scaling.minimum = new aw.Drawing.Charts.AxisBound(Date.parse("2017-11-05"));
xAxis.scaling.maximum = new aw.Drawing.Charts.AxisBound(Date.parse("2017-12-03"));

// Set the major units of the X-axis to a week, and the minor units to a day.
xAxis.baseTimeUnit = aw.Drawing.Charts.AxisTimeUnit.Days;
xAxis.majorUnit = 7.0;
xAxis.majorTickMark = aw.Drawing.Charts.AxisTickMark.Cross;
xAxis.minorUnit = 1.0;
xAxis.minorTickMark = aw.Drawing.Charts.AxisTickMark.Outside;
xAxis.hasMajorGridlines = true;
xAxis.hasMinorGridlines = true;

// Define Y-axis properties for decimal values.
let yAxis = chart.axisY;
yAxis.tickLabels.position = aw.Drawing.Charts.AxisTickLabelPosition.High;
yAxis.majorUnit = 100.0;
yAxis.minorUnit = 50.0;
yAxis.displayUnit.unit = aw.Drawing.Charts.AxisBuiltInUnit.Hundreds;
yAxis.scaling.minimum = new aw.Drawing.Charts.AxisBound(100);
yAxis.scaling.maximum = new aw.Drawing.Charts.AxisBound(700);
yAxis.hasMajorGridlines = true;
yAxis.hasMinorGridlines = true;

doc.save(base.artifactsDir + "Charts.DateTimeValues.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [AxisScaling](../)

