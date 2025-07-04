---
title: ImageSize.VerticalResolution
linktitle: VerticalResolution
articleTitle: VerticalResolution
second_title: Aspose.Words for .NET
description: Discover the ImageSize VerticalResolution property to easily access vertical DPI resolution, enhancing your image quality and performance.
type: docs
weight: 50
url: /net/aspose.words.drawing/imagesize/verticalresolution/
---
## ImageSize.VerticalResolution property

Gets the vertical resolution in DPI.

```csharp
public double VerticalResolution { get; }
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
