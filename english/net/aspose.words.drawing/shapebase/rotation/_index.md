---
title: ShapeBase.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words for .NET
description: Discover the ShapeBase Rotation property, easily define and customize rotation angles for your shapes, enhancing your design's precision and creativity.
type: docs
weight: 500
url: /net/aspose.words.drawing/shapebase/rotation/
---
## ShapeBase.Rotation property

Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle.

```csharp
public double Rotation { get; set; }
```

## Remarks

The default value is 0.

## Examples

Shows how to insert and rotate an image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a shape with an image.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// Rotate the image 45 degrees clockwise.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
