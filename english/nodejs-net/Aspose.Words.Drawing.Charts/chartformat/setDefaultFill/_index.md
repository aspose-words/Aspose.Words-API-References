---
title: ChartFormat.setDefaultFill method
linktitle: setDefaultFill method
articleTitle: setDefaultFill method
second_title: Aspose.Words for NodeJs
description: "ChartFormat.setDefaultFill method. Resets the fill of the chart element to have the default value."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartformat/setDefaultFill/
---

## setDefaultFill() {#default}

Resets the fill of the chart element to have the default value.


```js
setDefaultFill()
```

### Examples

Shows how to reset the fill to the default value defined in the series.

```js
let doc = new aw.Document(base.myDir + "DataPoint format.docx");

let shape = doc.getShape(0, true);
let series = shape.chart.series.at(0);
let dataPoint = series.dataPoints.at(1);

expect(dataPoint.format.isDefined).toEqual(true);

dataPoint.format.setDefaultFill();

doc.save(base.artifactsDir + "Charts.ResetDataPointFill.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartFormat](../)

