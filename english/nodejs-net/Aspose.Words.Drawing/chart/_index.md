---
title: Chart class
linktitle: Chart class
articleTitle: Chart class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Chart class. Provides access to the chart shape properties"
type: docs
weight: 60
url: /nodejs-net/aspose.words.drawing/chart/
---

## Chart class

Provides access to the chart shape properties.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/nodejs-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [axes](./axes/) | Gets a collection of all axes of this chart. |
| [axisX](./axisX/) | Provides access to properties of the primary X axis of the chart. |
| [axisY](./axisY/) | Provides access to properties of the primary Y axis of the chart. |
| [axisZ](./axisZ/) | Provides access to properties of the Z axis of the chart. |
| [dataTable](./dataTable/) | Provides access to properties of a data table of this chart. The data table can be shown using the [ChartDataTable.show](../../aspose.words.drawing.charts/chartdatatable/show/) property. |
| [format](./format/) | Provides access to fill and line formatting of the chart. |
| [legend](./legend/) | Provides access to the chart legend properties. |
| [series](./series/) | Provides access to series collection. |
| [seriesGroups](./seriesGroups/) | Provides access to a series group collection of this chart. |
| [sourceFullName](./sourceFullName/) | Gets the path and name of an xls/xlsx file this chart is linked to. |
| [title](./title/) | Provides access to the chart title properties. |

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

* module [Aspose.Words.Drawing](../)

