---
title: ChartTitle.show property
linktitle: show property
articleTitle: show property
second_title: Aspose.Words for Node.js
description: "ChartTitle.show property. Determines whether the title shall be shown for this chart"
type: docs
weight: 40
url: /nodejs-net/aspose.words.drawing.charts/charttitle/show/
---

## ChartTitle.show property

Determines whether the title shall be shown for this chart.
Default value is ``true``.



```js
get show(): boolean
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

