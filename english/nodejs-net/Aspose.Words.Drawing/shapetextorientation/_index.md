---
title: ShapeTextOrientation enumeration
linktitle: ShapeTextOrientation enumeration
articleTitle: ShapeTextOrientation enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.ShapeTextOrientation enumeration. Specifies orientation of text in shapes."
type: docs
weight: 410
url: /nodejs-net/aspose.words.drawing/shapetextorientation/
---

## ShapeTextOrientation enumeration

Specifies orientation of text in shapes.


### Members

| Name | Description |
| --- | --- |
| Horizontal | Text is arranged horizontally (lr-tb). |
| Downward | Text is rotated 90 degrees to the right to appear from top to bottom (tb-rl). |
| Upward | Text is rotated 90 degrees to the left to appear from bottom to top (bt-lr). |
| VerticalFarEast | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom (tb-rl-v). |
| VerticalRotatedFarEast | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom vertically, then left to right horizontally  (tb-lr-v). |
| WordArtVertical | Text is vertical, with one letter on top of the other. |
| WordArtVerticalRightToLeft | Text is vertical, with one letter on top of the other, then right to left horizontally. |

### Examples

Shows how to change orientation and rotation for data labels.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 432, 252);
let series = shape.chart.series.at(0);
let dataLabels = series.dataLabels;

// Show data labels.
series.hasDataLabels = true;
dataLabels.showValue = true;
dataLabels.showCategoryName = true;

// Define data label shape.
dataLabels.format.shapeType = aw.Drawing.Charts.ChartShapeType.UpArrow;
dataLabels.format.stroke.fill.solid("#00008B");

// Set data label orientation and rotation for the entire series.
dataLabels.orientation = aw.Drawing.ShapeTextOrientation.VerticalFarEast;
dataLabels.rotation = -45;

// Change orientation and rotation of the first data label.
dataLabels.at(0).orientation = aw.Drawing.ShapeTextOrientation.Horizontal;
dataLabels.at(0).rotation = 45;

doc.save(base.artifactsDir + "Charts.LabelOrientationRotation.docx");
```

### See Also

* module [Aspose.Words.Drawing](../)

