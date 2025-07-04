---
title: ImageSize.HeightPoints
linktitle: HeightPoints
articleTitle: HeightPoints
second_title: Aspose.Words for .NET
description: Discover the ImageSize HeightPoints property to easily retrieve image height in points—1 point equals 1/72 inch. Optimize your images effortlessly!
type: docs
weight: 30
url: /net/aspose.words.drawing/imagesize/heightpoints/
---
## ImageSize.HeightPoints property

Gets the height of the image in points. 1 point is 1/72 inch.

```csharp
public double HeightPoints { get; }
```

## Examples

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

* class [ImageSize](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
