---
title: ChartTitle class
linktitle: ChartTitle class
articleTitle: ChartTitle class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.ChartTitle class. Provides access to the chart title properties"
type: docs
weight: 390
url: /nodejs-net/aspose.words.drawing.charts/charttitle/
---

## ChartTitle class

Provides access to the chart title properties.
To learn more, visit the [Working with
            Charts](https://docs.aspose.com/words/nodejs-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [font](./font/) | Provides access to the font formatting of the chart title. |
| [format](./format/) | Provides access to fill and line formatting of the chart title. |
| [orientation](./orientation/) | Gets or sets the orientation of the chart title text. |
| [overlay](./overlay/) | Determines whether other chart elements shall be allowed to overlap title. By default overlay is ``false``. |
| [rotation](./rotation/) | Gets or sets the rotation of the chart title in degrees. |
| [show](./show/) | Determines whether the title shall be shown for this chart. Default value is ``true``. |
| [text](./text/) | Gets or sets the text of the chart title. If ``null`` or empty value is specified, auto generated title will be shown. |

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

* module [Aspose.Words.Drawing.Charts](../)

