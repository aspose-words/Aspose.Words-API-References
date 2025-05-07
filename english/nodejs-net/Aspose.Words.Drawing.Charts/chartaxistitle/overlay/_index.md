---
title: ChartAxisTitle.overlay property
linktitle: overlay property
articleTitle: overlay property
second_title: Aspose.Words for Node.js
description: "ChartAxisTitle.overlay property. Determines whether other chart elements shall be allowed to overlap the title"
type: docs
weight: 30
url: /nodejs-net/aspose.words.drawing.charts/chartaxistitle/overlay/
---

## ChartAxisTitle.overlay property

Determines whether other chart elements shall be allowed to overlap the title.
The default value is ``false``.



```js
get overlay(): boolean
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

