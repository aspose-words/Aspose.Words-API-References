---
title: Fill.Opacity
linktitle: Opacity
second_title: Aspose.Words for .NET API Reference
description: Fill Opacity property. Gets or sets the degree of opacity of the specified fill as a value between 0.0 clear and 1.0 opaque in C#.
type: docs
weight: 130
url: /net/aspose.words.drawing/fill/opacity/
---
## Opacity property

Gets or sets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque).

```csharp
public double Opacity { get; set; }
```

## Remarks

This property is the opposite of property [`Transparency`](../transparency/).

## Examples

Shows how to fill a shape with a solid color.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Write some text, and then cover it with a floating shape.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Use the "StrokeColor" property to set the color of the outline of the shape.
shape.StrokeColor = Color.CadetBlue;

// Use the "FillColor" property to set the color of the inside area of the shape.
shape.FillColor = Color.LightBlue;

// The "Opacity" property determines how transparent the color is on a 0-1 scale,
// with 1 being fully opaque, and 0 being invisible.
// The shape fill by default is fully opaque, so we cannot see the text that this shape is on top of.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Set the shape fill color's opacity to a lower value so that we can see the text underneath it.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### See Also

* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../fill/)
* assembly [Aspose.Words](../../../)
