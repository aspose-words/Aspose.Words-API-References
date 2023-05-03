---
title: ImageSize.WidthPoints
linktitle: WidthPoints
second_title: Aspose.Words for .NET API Reference
description: ImageSize WidthPoints property. Gets the width of the image in points. 1 point is 1/72 inch in C#.
type: docs
weight: 70
url: /net/aspose.words.drawing/imagesize/widthpoints/
---
## ImageSize.WidthPoints property

Gets the width of the image in points. 1 point is 1/72 inch.

```csharp
public double WidthPoints { get; }
```

## Examples

Shows how to resize a shape with an image.

```csharp
#if NET48 || JAVA
            Image image = Image.FromFile(ImageDir + "Logo.jpg");

            Assert.AreEqual(400, image.Size.Width);
            Assert.AreEqual(400, image.Size.Height);
#elif NET5_0_OR_GREATER
            SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg");

            Assert.AreEqual(400, image.Width);
            Assert.AreEqual(400, image.Height);
#endif

            // When we insert an image using the "InsertImage" method, the builder scales the shape that displays the image so that,
            // when we view the document using 100% zoom in Microsoft Word, the shape displays the image in its actual size.
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

            // A 400x400 image will create an ImageData object with an image size of 300x300pt.
            ImageSize imageSize = shape.ImageData.ImageSize;

            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // If a shape's dimensions match the image data's dimensions,
            // then the shape is displaying the image in its original size.
            Assert.AreEqual(300.0d, shape.Width);
            Assert.AreEqual(300.0d, shape.Height);

            // Reduce the overall size of the shape by 50%. 
            shape.Width *= 0.5;

            // Scaling factors apply to both the width and the height at the same time to preserve the shape's proportions. 
            Assert.AreEqual(150.0d, shape.Width);
            Assert.AreEqual(150.0d, shape.Height);

            // When we resize the shape, the size of the image data remains the same.
            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // We can reference the image data dimensions to apply a scaling based on the size of the image.
            shape.Width = imageSize.WidthPoints * 1.1;

            Assert.AreEqual(330.0d, shape.Width);
            Assert.AreEqual(330.0d, shape.Height);

            doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### See Also

* class [ImageSize](../)
* namespace [Aspose.Words.Drawing](../../imagesize/)
* assembly [Aspose.Words](../../../)
