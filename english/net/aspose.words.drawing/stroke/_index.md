---
title: Stroke Class
linktitle: Stroke
articleTitle: Stroke
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Stroke class. Defines a stroke for a shape in C#.
type: docs
weight: 1690
url: /net/aspose.words.drawing/stroke/
---
## Stroke class

Defines a stroke for a shape.

To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/net/working-with-shapes/) documentation article.

```csharp
public class Stroke
```

## Properties

| Name | Description |
| --- | --- |
| [BackColor](../../aspose.words.drawing/stroke/backcolor/) { get; set; } | Gets or sets the background color of the stroke. |
| [BackThemeColor](../../aspose.words.drawing/stroke/backthemecolor/) { get; set; } | Gets or sets a ThemeColor object that represents the stroke background color. |
| [BackTintAndShade](../../aspose.words.drawing/stroke/backtintandshade/) { get; set; } | Gets or sets a double value that lightens or darkens the stroke background color. |
| [BaseForeColor](../../aspose.words.drawing/stroke/baseforecolor/) { get; } | Gets the base foreground color of the stroke without any modifiers. |
| [Color](../../aspose.words.drawing/stroke/color/) { get; set; } | Defines the color of a stroke. |
| [Color2](../../aspose.words.drawing/stroke/color2/) { get; set; } | Defines a second color for a stroke. |
| [DashStyle](../../aspose.words.drawing/stroke/dashstyle/) { get; set; } | Specifies the dot and dash pattern for a stroke. |
| [EndArrowLength](../../aspose.words.drawing/stroke/endarrowlength/) { get; set; } | Defines the arrowhead length for the end of a stroke. |
| [EndArrowType](../../aspose.words.drawing/stroke/endarrowtype/) { get; set; } | Defines the arrowhead for the end of a stroke. |
| [EndArrowWidth](../../aspose.words.drawing/stroke/endarrowwidth/) { get; set; } | Defines the arrowhead width for the end of a stroke. |
| [EndCap](../../aspose.words.drawing/stroke/endcap/) { get; set; } | Defines the cap style for the end of a stroke. |
| [Fill](../../aspose.words.drawing/stroke/fill/) { get; } | Gets fill formatting for the `Stroke`. |
| [ForeColor](../../aspose.words.drawing/stroke/forecolor/) { get; set; } | Gets or sets the foreground color of the stroke. |
| [ForeThemeColor](../../aspose.words.drawing/stroke/forethemecolor/) { get; set; } | Gets or sets a ThemeColor object that represents the stroke foreground color. |
| [ForeTintAndShade](../../aspose.words.drawing/stroke/foretintandshade/) { get; set; } | Gets or sets a double value that lightens or darkens the stroke foreground color. |
| [ImageBytes](../../aspose.words.drawing/stroke/imagebytes/) { get; } | Defines the image for a stroke image or pattern fill. |
| [JoinStyle](../../aspose.words.drawing/stroke/joinstyle/) { get; set; } | Defines the join style of a polyline. |
| [LineStyle](../../aspose.words.drawing/stroke/linestyle/) { get; set; } | Defines the line style of the stroke. |
| [On](../../aspose.words.drawing/stroke/on/) { get; set; } | Defines whether the path will be stroked. |
| [Opacity](../../aspose.words.drawing/stroke/opacity/) { get; set; } | Defines the amount of transparency of a stroke. Valid range is from 0 to 1. |
| [StartArrowLength](../../aspose.words.drawing/stroke/startarrowlength/) { get; set; } | Defines the arrowhead length for the start of a stroke. |
| [StartArrowType](../../aspose.words.drawing/stroke/startarrowtype/) { get; set; } | Defines the arrowhead for the start of a stroke. |
| [StartArrowWidth](../../aspose.words.drawing/stroke/startarrowwidth/) { get; set; } | Defines the arrowhead width for the start of a stroke. |
| [Transparency](../../aspose.words.drawing/stroke/transparency/) { get; set; } | Gets or sets a value between 0.0 (opaque) and 1.0 (clear) representing the degree of transparency of the stroke. |
| [Visible](../../aspose.words.drawing/stroke/visible/) { get; set; } | Gets or sets a flag indicating whether the stroke is visible. |
| [Weight](../../aspose.words.drawing/stroke/weight/) { get; set; } | Defines the brush thickness that strokes the path of a shape in points. |

## Remarks

Use the [`Stroke`](../shape/stroke/) property to access stroke properties of a shape. You do not create instances of the `Stroke` class directly.

## Examples

Shows how change stroke properties.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Basic shapes, such as the rectangle, have two visible parts.
// 1 -  The fill, which applies to the area within the outline of the shape:
shape.Fill.ForeColor = Color.White;

// 2 -  The stroke, which marks the outline of the shape:
// Modify various properties of this shape's stroke.
Stroke stroke = shape.Stroke;
stroke.On = true;
stroke.Weight = 5;
stroke.Color = Color.Red;
stroke.DashStyle = DashStyle.ShortDashDotDot;
stroke.JoinStyle = JoinStyle.Miter;
stroke.EndCap = EndCap.Square;
stroke.LineStyle = ShapeLineStyle.Triple;
stroke.Fill.TwoColorGradient(Color.Red, Color.Blue, GradientStyle.Vertical, GradientVariant.Variant1);

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
