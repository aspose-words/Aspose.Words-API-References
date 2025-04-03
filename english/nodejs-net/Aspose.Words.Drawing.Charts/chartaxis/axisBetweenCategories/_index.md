---
title: ChartAxis.axisBetweenCategories property
linktitle: axisBetweenCategories property
articleTitle: axisBetweenCategories property
second_title: Aspose.Words for NodeJs
description: "ChartAxis.axisBetweenCategories property. Gets or sets a flag indicating whether the value axis crosses the category axis between categories."
type: docs
weight: 10
url: /nodejs-net/aspose.words.drawing.charts/chartaxis/axisBetweenCategories/
---

## ChartAxis.axisBetweenCategories property

Gets or sets a flag indicating whether the value axis crosses the category axis between categories.


```js
get axisBetweenCategories(): boolean
```

### Remarks

The property has effect only for value axes. It is not supported by MS Office 2016 new charts.


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

