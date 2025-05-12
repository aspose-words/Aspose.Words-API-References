---
title: AxisTickLabels.orientation property
linktitle: orientation property
articleTitle: orientation property
second_title: Aspose.Words for Node.js
description: "AxisTickLabels.orientation property. Gets or sets the orientation of the tick label text."
type: docs
weight: 50
url: /nodejs-net/aspose.words.drawing.charts/axisticklabels/orientation/
---

## AxisTickLabels.orientation property

Gets or sets the orientation of the tick label text.


```js
get orientation(): Aspose.Words.Drawing.ShapeTextOrientation
```

### Remarks

The default value is [ShapeTextOrientation.Horizontal](../../../aspose.words.drawing/shapetextorientation/#Horizontal).

Note that some [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/) values do not affect the orientation of tick label text
in value axes.




### Examples

Shows how to change orientation and rotation for axis tick labels.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a column chart.
let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 432, 252);
let xTickLabels = shape.chart.axisX.tickLabels;
let yTickLabels = shape.chart.axisY.tickLabels;

// Set axis tick label orientation and rotation.
xTickLabels.orientation = aw.Drawing.ShapeTextOrientation.VerticalFarEast;
xTickLabels.rotation = -30;
yTickLabels.orientation = aw.Drawing.ShapeTextOrientation.Horizontal;
yTickLabels.rotation = 45;

doc.save(base.artifactsDir + "Charts.TickLabelsOrientationRotation.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [AxisTickLabels](../)

