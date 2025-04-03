---
title: Stroke class
linktitle: Stroke class
articleTitle: Stroke class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Stroke class. Defines a stroke for a shape"
type: docs
weight: 450
url: /nodejs-net/aspose.words.drawing/stroke/
---

## Stroke class

Defines a stroke for a shape.
To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/nodejs-net/working-with-shapes/) documentation article.




### Remarks

Use the [Shape.stroke](../shape/stroke/) property to access stroke properties of a shape.
You do not create instances of the [Stroke](./) class directly.




### Properties

| Name | Description |
| --- | --- |
| [backColor](./backColor/) | Gets or sets the background color of the stroke. |
| [backThemeColor](./backThemeColor/) | Gets or sets a ThemeColor object that represents the stroke background color. |
| [backTintAndShade](./backTintAndShade/) | Gets or sets a double value that lightens or darkens the stroke background color. |
| [baseForeColor](./baseForeColor/) | Gets the base foreground color of the stroke without any modifiers. |
| [color](./color/) | Defines the color of a stroke. |
| [color2](./color2/) | Defines a second color for a stroke. |
| [dashStyle](./dashStyle/) | Specifies the dot and dash pattern for a stroke. |
| [endArrowLength](./endArrowLength/) | Defines the arrowhead length for the end of a stroke. |
| [endArrowType](./endArrowType/) | Defines the arrowhead for the end of a stroke. |
| [endArrowWidth](./endArrowWidth/) | Defines the arrowhead width for the end of a stroke. |
| [endCap](./endCap/) | Defines the cap style for the end of a stroke. |
| [fill](./fill/) | Gets fill formatting for the [Stroke](./). |
| [foreColor](./foreColor/) | Gets or sets the foreground color of the stroke. |
| [foreThemeColor](./foreThemeColor/) | Gets or sets a ThemeColor object that represents the stroke foreground color. |
| [foreTintAndShade](./foreTintAndShade/) | Gets or sets a double value that lightens or darkens the stroke foreground color. |
| [imageBytes](./imageBytes/) | Defines the image for a stroke image or pattern fill. |
| [joinStyle](./joinStyle/) | Defines the join style of a polyline. |
| [lineStyle](./lineStyle/) | Defines the line style of the stroke. |
| [on](./on/) | Defines whether the path will be stroked. |
| [opacity](./opacity/) | Defines the amount of transparency of a stroke. Valid range is from 0 to 1. |
| [startArrowLength](./startArrowLength/) | Defines the arrowhead length for the start of a stroke. |
| [startArrowType](./startArrowType/) | Defines the arrowhead for the start of a stroke. |
| [startArrowWidth](./startArrowWidth/) | Defines the arrowhead width for the start of a stroke. |
| [transparency](./transparency/) | Gets or sets a value between 0.0 (opaque) and 1.0 (clear) representing the degree of transparency of the stroke. |
| [visible](./visible/) | Gets or sets a flag indicating whether the stroke is visible. |
| [weight](./weight/) | Defines the brush thickness that strokes the path of a shape in points. |

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
* property [Shape.stroke](../shape/stroke/)

