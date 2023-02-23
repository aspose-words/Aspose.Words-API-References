---
title: ShapeLineStyle Enum
linktitle: ShapeLineStyle
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Drawing.ShapeLineStyle enum. Specifies the compound line style of a Shape in C#.
type: docs
weight: 1120
url: /net/aspose.words.drawing/shapelinestyle/
---
## ShapeLineStyle enumeration

Specifies the compound line style of a [`Shape`](../shape/).

```csharp
public enum ShapeLineStyle
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Single | `0` | Single line. |
| Double | `1` | Double lines of equal width. |
| ThickThin | `2` | Double lines, one thick, one thin. |
| ThinThick | `3` | Double lines, one thin, one thick. |
| Triple | `4` | Three lines, thin, thick, thin. |
| Default | `0` | Default value is Single. |

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

* property [LineStyle](../stroke/linestyle/)
* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
