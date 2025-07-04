---
title: ShapeBase.FlipOrientation
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words for .NET
description: Discover the ShapeBase FlipOrientation property to effortlessly switch your shape's orientation, enhancing your designs with ease and creativity.
type: docs
weight: 180
url: /net/aspose.words.drawing/shapebase/fliporientation/
---
## ShapeBase.FlipOrientation property

Switches the orientation of a shape.

```csharp
public FlipOrientation FlipOrientation { get; set; }
```

## Remarks

The default value is None.

## Examples

Shows how to flip a shape on an axis.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert an image shape and leave its orientation in its default state.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

Assert.That(shape.FlipOrientation, Is.EqualTo(FlipOrientation.None));

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the second shape on the y-axis,
// making it into a horizontal mirror image of the first shape.
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the third shape on the x-axis,
// making it into a vertical mirror image of the first shape.
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the fourth shape on both the x and y axes,
// making it into a horizontal and vertical mirror image of the first shape.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### See Also

* enum [FlipOrientation](../../fliporientation/)
* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
