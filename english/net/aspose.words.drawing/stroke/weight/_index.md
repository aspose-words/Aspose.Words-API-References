---
title: Stroke.Weight
linktitle: Weight
articleTitle: Weight
second_title: Aspose.Words for .NET
description: Stroke Weight property. Defines the brush thickness that strokes the path of a shape in points in C#.
type: docs
weight: 210
url: /net/aspose.words.drawing/stroke/weight/
---
## Stroke.Weight property

Defines the brush thickness that strokes the path of a shape in points.

```csharp
public double Weight { get; set; }
```

## Remarks

The default value for a [`Shape`](../../shape/) is 0.75.

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

* class [Stroke](../)
* namespace [Aspose.Words.Drawing](../../stroke/)
* assembly [Aspose.Words](../../../)
