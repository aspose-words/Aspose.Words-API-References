---
title: ChartLegend.overlay property
linktitle: overlay property
articleTitle: overlay property
second_title: Aspose.Words for Node.js
description: "ChartLegend.overlay property. Determines whether other chart elements shall be allowed to overlap legend"
type: docs
weight: 40
url: /nodejs-net/aspose.words.drawing.charts/chartlegend/overlay/
---

## ChartLegend.overlay property

Determines whether other chart elements shall be allowed to overlap legend.
Default value is ``false``.



```js
get overlay(): boolean
```

### Examples

Shows how to edit the appearance of a chart's legend.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Line, 450, 300);
let chart = shape.chart;

expect(chart.series.count).toEqual(3);
expect(chart.series.at(0).name).toEqual("Series 1");
expect(chart.series.at(1).name).toEqual("Series 2");
expect(chart.series.at(2).name).toEqual("Series 3");

// Move the chart's legend to the top right corner.
let legend = chart.legend;
legend.position = aw.Drawing.Charts.LegendPosition.TopRight;

// Give other chart elements, such as the graph, more room by allowing them to overlap the legend.
legend.overlay = true;

doc.save(base.artifactsDir + "Charts.ChartLegend.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartLegend](../)

