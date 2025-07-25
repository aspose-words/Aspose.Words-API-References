---
title: ShapeBase.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words for .NET
description: Discover the ShapeBase Width property. Easily adjust the width of your shape's containing block for enhanced design flexibility and precision.
type: docs
weight: 610
url: /net/aspose.words.drawing/shapebase/width/
---
## ShapeBase.Width property

Gets or sets the width of the containing block of the shape.

```csharp
public double Width { get; set; }
```

## Remarks

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

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

Assert.That(shape.Width, Is.EqualTo(125.0d));

// The "Bottom" and "Right" properties contain the bottom and right edges of the image.
Assert.That(shape.Bottom, Is.EqualTo(shape.Top + shape.Height));
Assert.That(shape.Right, Is.EqualTo(shape.Left + shape.Width));

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

Shows how to resize a shape with an image.

```csharp
// When we insert an image using the "InsertImage" method, the builder scales the shape that displays the image so that,
// when we view the document using 100% zoom in Microsoft Word, the shape displays the image in its actual size.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// A 400x400 image will create an ImageData object with an image size of 300x300pt.
ImageSize imageSize = shape.ImageData.ImageSize;

Assert.That(imageSize.WidthPoints, Is.EqualTo(300.0d));
Assert.That(imageSize.HeightPoints, Is.EqualTo(300.0d));

// If a shape's dimensions match the image data's dimensions,
// then the shape is displaying the image in its original size.
Assert.That(shape.Width, Is.EqualTo(300.0d));
Assert.That(shape.Height, Is.EqualTo(300.0d));

// Reduce the overall size of the shape by 50%. 
shape.Width *= 0.5;

// Scaling factors apply to both the width and the height at the same time to preserve the shape's proportions. 
Assert.That(shape.Width, Is.EqualTo(150.0d));
Assert.That(shape.Height, Is.EqualTo(150.0d));

// When we resize the shape, the size of the image data remains the same.
Assert.That(imageSize.WidthPoints, Is.EqualTo(300.0d));
Assert.That(imageSize.HeightPoints, Is.EqualTo(300.0d));

// We can reference the image data dimensions to apply a scaling based on the size of the image.
shape.Width = imageSize.WidthPoints * 1.1;

Assert.That(shape.Width, Is.EqualTo(330.0d));
Assert.That(shape.Height, Is.EqualTo(330.0d));

doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
