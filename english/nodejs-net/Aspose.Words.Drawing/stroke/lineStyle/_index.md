---
title: Stroke.lineStyle property
linktitle: lineStyle property
articleTitle: lineStyle property
second_title: Aspose.Words for Node.js
description: "Stroke.lineStyle property. Defines the line style of the stroke."
type: docs
weight: 180
url: /nodejs-net/aspose.words.drawing/stroke/lineStyle/
---

## Stroke.lineStyle property

Defines the line style of the stroke.


```js
get lineStyle(): Aspose.Words.Drawing.ShapeLineStyle
```

### Remarks

The default value is [ShapeLineStyle.Single](../../shapelinestyle/#Single).




### Examples

Shows how change stroke properties.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertShape(aw.Drawing.ShapeType.Rectangle, aw.Drawing.RelativeHorizontalPosition.LeftMargin, 100,
  aw.Drawing.RelativeVerticalPosition.TopMargin, 100, 200, 200, aw.Drawing.WrapType.None);

// Basic shapes, such as the rectangle, have two visible parts.
// 1 -  The fill, which applies to the area within the outline of the shape:
shape.fill.foreColor = "#FFFFFF";

// 2 -  The stroke, which marks the outline of the shape:
// Modify various properties of this shape's stroke.
let stroke = shape.stroke;
stroke.on = true;
stroke.weight = 5;
stroke.color = "#FF0000";
stroke.dashStyle = aw.Drawing.DashStyle.ShortDashDotDot;
stroke.joinStyle = aw.Drawing.JoinStyle.Miter;
stroke.endCap = aw.Drawing.EndCap.Square;
stroke.lineStyle = aw.Drawing.ShapeLineStyle.Triple;
stroke.fill.twoColorGradient("#FF0000", "#0000FF", aw.Drawing.GradientStyle.Vertical, aw.Drawing.GradientVariant.Variant1);

doc.save(base.artifactsDir + "Shape.stroke.docx");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [Stroke](../)

