---
title: ShapeLineStyle enumeration
linktitle: ShapeLineStyle enumeration
articleTitle: ShapeLineStyle enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.ShapeLineStyle enumeration. Specifies the compound line style of a [Shape](../shape/)."
type: docs
weight: 390
url: /nodejs-net/aspose.words.drawing/shapelinestyle/
---

## ShapeLineStyle enumeration

Specifies the compound line style of a [Shape](../shape/).



### Members

| Name | Description |
| --- | --- |
| Single | Single line. |
| Double | Double lines of equal width. |
| ThickThin | Double lines, one thick, one thin. |
| ThinThick | Double lines, one thin, one thick. |
| Triple | Three lines, thin, thick, thin. |
| Default | Default value is [ShapeLineStyle.Single](./#Single). |

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

* module [Aspose.Words.Drawing](../)
* property [Stroke.lineStyle](../stroke/lineStyle/)

