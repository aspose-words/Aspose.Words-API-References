---
title: ShapeBase.CanHaveImage
linktitle: CanHaveImage
articleTitle: CanHaveImage
second_title: Aspose.Words for .NET
description: Discover the ShapeBase CanHaveImage property—learn how to determine if your shape type supports images for enhanced visual appeal!
type: docs
weight: 100
url: /net/aspose.words.drawing/shapebase/canhaveimage/
---
## ShapeBase.CanHaveImage property

Returns `true` if the shape type allows the shape to have an image.

```csharp
public bool CanHaveImage { get; }
```

## Remarks

Although Microsoft Word has a special shape type for images, it appears that in Microsoft Word documents any shape except a group shape can have an image, therefore this property returns `true` for all shapes except [`GroupShape`](../../groupshape/).

## Examples

Shows how to insert and rotate an image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a shape with an image.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.That(shape.CanHaveImage, Is.True);
Assert.That(shape.HasImage, Is.True);

// Rotate the image 45 degrees clockwise.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
