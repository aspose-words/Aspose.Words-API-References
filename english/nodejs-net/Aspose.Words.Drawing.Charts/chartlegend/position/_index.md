﻿---
title: ChartLegend.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Node.js
description: "ChartLegend.position property. Specifies the position of the legend on a chart."
type: docs
weight: 50
url: /nodejs-net/aspose.words.drawing.charts/chartlegend/position/
---

## ChartLegend.position property

Specifies the position of the legend on a chart.


```js
get position(): Aspose.Words.Drawing.Charts.LegendPosition
```

### Remarks

The default value is [LegendPosition.Right](../../legendposition/#Right) for pre-Word 2016 charts and
[LegendPosition.Top](../../legendposition/#Top) for Word 2016 charts.



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

