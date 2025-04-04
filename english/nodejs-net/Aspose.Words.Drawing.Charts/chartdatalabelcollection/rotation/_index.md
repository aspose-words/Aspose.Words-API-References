---
title: ChartDataLabelCollection.rotation property
linktitle: rotation property
articleTitle: rotation property
second_title: Aspose.Words for Node.js
description: "ChartDataLabelCollection.rotation property. Gets or sets the rotation of the data labels of the entire series in degrees."
type: docs
weight: 70
url: /nodejs-net/aspose.words.drawing.charts/chartdatalabelcollection/rotation/
---

## ChartDataLabelCollection.rotation property

Gets or sets the rotation of the data labels of the entire series in degrees.


```js
get rotation(): number
```

### Remarks

The range of acceptable values is from -180 to 180 inclusive. The default value is 0.

If the [ChartDataLabelCollection.orientation](../orientation/) value is [ShapeTextOrientation.Horizontal](../../../aspose.words.drawing/shapetextorientation/#Horizontal), label shapes,
if they exist, are rotated along with the label text. Otherwise, only the label text is rotated.




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

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartDataLabelCollection](../)

