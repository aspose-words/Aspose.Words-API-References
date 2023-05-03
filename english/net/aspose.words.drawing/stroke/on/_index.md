---
title: Stroke.On
linktitle: On
second_title: Aspose.Words for .NET API Reference
description: Stroke On property. Defines whether the path will be stroked in C#.
type: docs
weight: 140
url: /net/aspose.words.drawing/stroke/on/
---
## Stroke.On property

Defines whether the path will be stroked.

```csharp
public bool On { get; set; }
```

## Remarks

The default value for a [`Shape`](../../shape/) is `true`.

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

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### See Also

* class [Stroke](../)
* namespace [Aspose.Words.Drawing](../../stroke/)
* assembly [Aspose.Words](../../../)
