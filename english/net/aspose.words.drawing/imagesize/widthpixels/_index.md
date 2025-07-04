---
title: ImageSize.WidthPixels
linktitle: WidthPixels
articleTitle: WidthPixels
second_title: Aspose.Words for .NET
description: Discover the ImageSize WidthPixels property to easily retrieve the pixel width of your images, enhancing your image management and optimization.
type: docs
weight: 60
url: /net/aspose.words.drawing/imagesize/widthpixels/
---
## ImageSize.WidthPixels property

Gets the width of the image in pixels.

```csharp
public int WidthPixels { get; }
```

## Examples

Shows how to read the properties of an image in a shape.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a shape into the document which contains an image taken from our local file system.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// If the shape contains an image, its ImageData property will be valid,
// and it will contain an ImageSize object.
ImageSize imageSize = shape.ImageData.ImageSize;

// The ImageSize object contains read-only information about the image within the shape.
Assert.That(imageSize.HeightPixels, Is.EqualTo(400));
Assert.That(imageSize.WidthPixels, Is.EqualTo(400));

const double delta = 0.05;
Assert.That(imageSize.HorizontalResolution, Is.EqualTo(95.98d).Within(delta));
Assert.That(imageSize.VerticalResolution, Is.EqualTo(95.98d).Within(delta));

// We can base the size of the shape on the size of its image to avoid stretching the image.
shape.Width = imageSize.WidthPoints * 2;
shape.Height = imageSize.HeightPoints * 2;

doc.Save(ArtifactsDir + "Drawing.ImageSize.docx");
```

### See Also

* class [ImageSize](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
