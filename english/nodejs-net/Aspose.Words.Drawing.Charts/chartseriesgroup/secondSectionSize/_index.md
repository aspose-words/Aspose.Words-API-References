---
title: ChartSeriesGroup.secondSectionSize property
linktitle: secondSectionSize property
articleTitle: secondSectionSize property
second_title: Aspose.Words for Node.js
description: "ChartSeriesGroup.secondSectionSize property. Gets or sets the size of the pie chart secondary section as a percentage."
type: docs
weight: 90
url: /nodejs-net/aspose.words.drawing.charts/chartseriesgroup/secondSectionSize/
---

## ChartSeriesGroup.secondSectionSize property

Gets or sets the size of the pie chart secondary section as a percentage.


```js
get secondSectionSize(): number
```

### Remarks

Applies to series groups of the [ChartSeriesType.PieOfPie](../../chartseriestype/#PieOfPie) and
[ChartSeriesType.PieOfBar](../../chartseriestype/#PieOfBar) types.

The range of acceptable values is from 5 to 200 inclusive. The default value is 75.




### Examples

Shows how to create and format pie of Pie chart.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.PieOfPie, 440, 300);
let chart = shape.chart;
// Delete the default generated series.
chart.series.clear();

let categories = [ "Category 1", "Category 2", "Category 3", "Category 4" ];
chart.series.add("Series 1", categories, [ 11, 8, 4, 3 ]);

// Format the Pie of Pie chart.
let seriesGroup = chart.seriesGroups.at(0);
seriesGroup.gapWidth = 10;
seriesGroup.secondSectionSize = 77;

doc.save(base.artifactsDir + "Charts.PieOfPieChart.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartSeriesGroup](../)

