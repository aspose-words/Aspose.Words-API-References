---
title: ShapeBase.Rotation
second_title: Aspose.Words for .NET API Reference
description: ShapeBase property. Defines the angle in degrees that a shape is rotated. Positive value corresponds to clockwise rotation angle in C#.
type: docs
weight: 430
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
Shape shape = builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// Rotate the image 45 degrees clockwise.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../shapebase/)
* assembly [Aspose.Words](../../../)
