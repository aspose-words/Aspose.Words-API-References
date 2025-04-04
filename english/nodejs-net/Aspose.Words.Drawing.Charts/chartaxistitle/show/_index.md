---
title: ChartAxisTitle.show property
linktitle: show property
articleTitle: show property
second_title: Aspose.Words for Node.js
description: "ChartAxisTitle.show property. Determines whether the title shall be shown for the axis"
type: docs
weight: 40
url: /nodejs-net/aspose.words.drawing.charts/chartaxistitle/show/
---

## ChartAxisTitle.show property

Determines whether the title shall be shown for the axis.
The default value is ``false``.



```js
get show(): boolean
```

### Examples

Shows how to set chart axis title.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 432, 252);

let chart = shape.chart;
let seriesColl = chart.series;
// Delete default generated series.
seriesColl.clear();

seriesColl.add("AW Series 1", [ "AW Category 1", "AW Category 2" ], [ 1, 2 ]);

let chartAxisXTitle = chart.axisX.title;
chartAxisXTitle.text = "Categories";
chartAxisXTitle.show = true;
let chartAxisYTitle = chart.axisY.title;
chartAxisYTitle.text = "Values";
chartAxisYTitle.show = true;
chartAxisYTitle.overlay = true;
chartAxisYTitle.font.size = 12;
chartAxisYTitle.font.color = "#0000FF";

doc.save(base.artifactsDir + "Charts.chartAxisTitle.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartAxisTitle](../)

