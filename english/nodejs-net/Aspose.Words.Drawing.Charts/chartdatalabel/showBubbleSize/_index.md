---
title: ChartDataLabel.showBubbleSize property
linktitle: showBubbleSize property
articleTitle: showBubbleSize property
second_title: Aspose.Words for NodeJs
description: "ChartDataLabel.showBubbleSize property. Allows to specify if bubble size is to be displayed for the data labels on a chart"
type: docs
weight: 130
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartdatalabel/showBubbleSize/
---

## ChartDataLabel.showBubbleSize property

Allows to specify if bubble size is to be displayed for the data labels on a chart. 
Applies only to Bubble charts. 
Default value is ``false``.



```js
get showBubbleSize(): boolean
```

### Examples

Shows how to use 3D effects with bubble charts.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Bubble3D, 500, 350);
let chart = shape.chart;

expect(chart.series.count).toEqual(1);
expect(chart.series.at(0).name).toEqual("Y-Values");
expect(chart.series.at(0).bubble3D).toEqual(true);

// Apply a data label to each bubble that displays its diameter.
for (let i = 0; i < 3; i++)
{
  chart.series.at(0).hasDataLabels = true;
  chart.series.at(0).dataLabels.at(i).showBubbleSize = true;
  chart.series.at(0).dataLabels.at(i).font.size = 12;
}

doc.save(base.artifactsDir + "Charts.bubble3D.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartDataLabel](../)

