---
title: AxisTickLabels.rotation property
linktitle: rotation property
articleTitle: rotation property
second_title: Aspose.Words for Node.js
description: "AxisTickLabels.rotation property. Gets or sets the rotation of the tick labels in degrees."
type: docs
weight: 70
url: /nodejs-net/aspose.words.drawing.charts/axisticklabels/rotation/
---

## AxisTickLabels.rotation property

Gets or sets the rotation of the tick labels in degrees.


```js
get rotation(): number
```

### Remarks

The range of acceptable values is from -180 to 180 inclusive. The default value is 0.


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

