---
title: ChartSeriesGroup.doughnutHoleSize property
linktitle: doughnutHoleSize property
articleTitle: doughnutHoleSize property
second_title: Aspose.Words for Node.js
description: "ChartSeriesGroup.doughnutHoleSize property. Gets or sets the hole size of the parent doughnut chart as a percentage."
type: docs
weight: 50
url: /nodejs-net/aspose.words.drawing.charts/chartseriesgroup/doughnutHoleSize/
---

## ChartSeriesGroup.doughnutHoleSize property

Gets or sets the hole size of the parent doughnut chart as a percentage.


```js
get doughnutHoleSize(): number
```

### Remarks

Applies only to series groups of the [ChartSeriesType.Doughnut](../../chartseriestype/#Doughnut) type.

The range of acceptable values is from 0 to 90 inclusive. The default value is 75.




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

