---
title: ChartTitle.overlay property
linktitle: overlay property
articleTitle: overlay property
second_title: Aspose.Words for Node.js
description: "ChartTitle.overlay property. Determines whether other chart elements shall be allowed to overlap title"
type: docs
weight: 30
url: /nodejs-net/aspose.words.drawing.charts/charttitle/overlay/
---

## ChartTitle.overlay property

Determines whether other chart elements shall be allowed to overlap title.
By default overlay is ``false``.



```js
get overlay(): boolean
```

### Examples

Shows how to insert a chart and set a title.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a chart shape with a document builder and get its chart.
let chartShape = builder.insertChart(aw.Drawing.Charts.ChartType.Bar, 400, 300);
let chart = chartShape.chart;

// Use the "Title" property to give our chart a title, which appears at the top center of the chart area.
let title = chart.title;
title.text = "My Chart";
title.font.size = 15;
title.font.color = "#008000";

// Set the "Show" property to "true" to make the title visible. 
title.show = true;

// Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
title.overlay = true;

doc.save(base.artifactsDir + "Charts.chartTitle.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartTitle](../)

