---
title: Stroke.Fill
linktitle: Fill
second_title: Aspose.Words for .NET API Reference
description: Stroke Fill property. Gets fill formatting for the Stroke in C#.
type: docs
weight: 90
url: /net/aspose.words.drawing/stroke/fill/
---
## Stroke.Fill property

Gets fill formatting for the [`Stroke`](../).

```csharp
public Fill Fill { get; }
```

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

* class [Fill](../../fill/)
* class [Stroke](../)
* namespace [Aspose.Words.Drawing](../../stroke/)
* assembly [Aspose.Words](../../../)
