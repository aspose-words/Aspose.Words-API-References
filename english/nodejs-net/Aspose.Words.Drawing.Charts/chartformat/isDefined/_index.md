---
title: ChartFormat.isDefined property
linktitle: isDefined property
articleTitle: isDefined property
second_title: Aspose.Words for Node.js
description: "ChartFormat.isDefined property. Gets a flag indicating whether any format is defined."
type: docs
weight: 20
url: /nodejs-net/aspose.words.drawing.charts/chartformat/isDefined/
---

## ChartFormat.isDefined property

Gets a flag indicating whether any format is defined.


```js
get isDefined(): boolean
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

