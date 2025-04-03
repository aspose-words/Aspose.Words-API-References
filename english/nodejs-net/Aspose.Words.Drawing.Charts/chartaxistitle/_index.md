---
title: ChartAxisTitle class
linktitle: ChartAxisTitle class
articleTitle: ChartAxisTitle class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Charts.ChartAxisTitle class. Provides access to the axis title properties"
type: docs
weight: 160
url: /nodejs-net/aspose.words.drawing.charts/chartaxistitle/
---

## ChartAxisTitle class

Provides access to the axis title properties.
To learn more, visit the [Working with
            Charts](https://docs.aspose.com/words/nodejs-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [font](./font/) | Provides access to the font formatting of the axis title. |
| [format](./format/) | Provides access to fill and line formatting of the axis title. |
| [overlay](./overlay/) | Determines whether other chart elements shall be allowed to overlap the title. The default value is ``false``. |
| [show](./show/) | Determines whether the title shall be shown for the axis. The default value is ``false``. |
| [text](./text/) | Gets or sets the text of the axis title. If ``null`` or empty value is specified, auto generated title will be shown. |

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

* module [Aspose.Words.Drawing.Charts](../)

