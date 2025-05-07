---
title: ChartSeriesGroup.firstSliceAngle property
linktitle: firstSliceAngle property
articleTitle: firstSliceAngle property
second_title: Aspose.Words for Node.js
description: "ChartSeriesGroup.firstSliceAngle property. Gets or sets the angle, in degrees, of the first slice of the parent pie chart."
type: docs
weight: 60
url: /nodejs-net/aspose.words.drawing.charts/chartseriesgroup/firstSliceAngle/
---

## ChartSeriesGroup.firstSliceAngle property

Gets or sets the angle, in degrees, of the first slice of the parent pie chart.


```js
get firstSliceAngle(): number
```

### Remarks

Applies to series groups of the [ChartSeriesType.Pie](../../chartseriestype/#Pie), [ChartSeriesType.Pie3D](../../chartseriestype/#Pie3D)
and [ChartSeriesType.Doughnut](../../chartseriestype/#Doughnut) types.

The range of acceptable values is from 0 to 360 inclusive. The default value is 0.




### Examples

Shows how to create and format Doughnut chart.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Doughnut, 400, 400);
let chart = shape.chart;
// Delete the default generated series.
chart.series.clear();

let categories = [ "Category 1", "Category 2", "Category 3" ];
chart.series.add("Series 1", categories, [ 4, 2, 5 ]);

// Format the Doughnut chart.
let seriesGroup = chart.seriesGroups.at(0);
seriesGroup.doughnutHoleSize = 10;
seriesGroup.firstSliceAngle = 270;

doc.save(base.artifactsDir + "Charts.doughnutChart.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartSeriesGroup](../)

