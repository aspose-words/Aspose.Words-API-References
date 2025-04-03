---
title: Chart.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for NodeJs
description: "Chart.title property. Provides access to the chart title properties."
type: docs
weight: 110
url: /nodejs-net/aspose.words.drawing/chart/title/
---

## Chart.title property

Provides access to the chart title properties.


```js
get title(): Aspose.Words.Drawing.Charts.ChartTitle
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

* module [Aspose.Words.Drawing](../../)
* class [Chart](../)

