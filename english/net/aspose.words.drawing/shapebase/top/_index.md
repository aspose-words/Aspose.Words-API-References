---
title: ShapeBase.Top
second_title: Aspose.Words for .NET API Reference
description: ShapeBase property. Gets or sets the position of the top edge of the containing block of the shape in C#.
type: docs
weight: 500
url: /net/aspose.words.drawing/shapebase/top/
---
## ShapeBase.Top property

Gets or sets the position of the top edge of the containing block of the shape.

```csharp
public double Top { get; set; }
```

## Remarks

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

Has effect only for floating shapes.

## Examples

Shows how to insert a floating image, and specify its position and size.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
// as the shape's horizontal distance, in points, from the left side of the page. 
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Set the shape's horizontal distance from the left side of the page to 100.
shape.Left = 100;

// Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Set the shape's height, which will automatically scale the width to preserve dimensions.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// The "Bottom" and "Right" properties contain the bottom and right edges of the image.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../shapebase/)
* assembly [Aspose.Words](../../../)
