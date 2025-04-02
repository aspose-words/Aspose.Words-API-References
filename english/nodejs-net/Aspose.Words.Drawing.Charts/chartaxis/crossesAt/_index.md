---
title: ChartAxis.crossesAt property
linktitle: crossesAt property
articleTitle: crossesAt property
second_title: Aspose.Words for NodeJs
description: "ChartAxis.crossesAt property. Specifies where on the perpendicular axis the axis crosses."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartaxis/crossesAt/
---

## ChartAxis.crossesAt property

Specifies where on the perpendicular axis the axis crosses.


```js
get crossesAt(): number
```

### Remarks

The property has effect only if [ChartAxis.crosses](../crosses/) are set to [AxisCrosses.Custom](../../axiscrosses/#Custom).
It is not supported by MS Office 2016 new charts.

The units are determined by the type of axis. When the axis is a value axis, the value of the property
is a decimal number on the value axis. When the axis is a time category axis, the value is defined as
an integer number of days relative to the base date (30/12/1899). For a text category axis, the value is
an integer category number, starting with 1 as the first category.




### Examples

Shows how to get a graph axis to cross at a custom location.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 450, 250);
let chart = shape.chart;

expect(chart.series.count).toEqual(3);
expect(chart.series.at(0).name).toEqual("Series 1");
expect(chart.series.at(1).name).toEqual("Series 2");
expect(chart.series.at(2).name).toEqual("Series 3");

// For column charts, the Y-axis crosses at zero by default,
// which means that columns for all values below zero point down to represent negative values.
// We can set a different value for the Y-axis crossing. In this case, we will set it to 3.
let axis = chart.axisX;
axis.crosses = aw.Drawing.Charts.AxisCrosses.Custom;
axis.crossesAt = 3;
axis.axisBetweenCategories = true;

doc.save(base.artifactsDir + "Charts.AxisCross.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartAxis](../)

