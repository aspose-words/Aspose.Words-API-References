---
title: ImageSaveOptions.PixelFormat
linktitle: PixelFormat
articleTitle: PixelFormat
second_title: Aspose.Words for .NET
description: Discover the ImageSaveOptions PixelFormat property to easily customize the pixel format of your generated images for optimal quality and performance.
type: docs
weight: 130
url: /net/aspose.words.saving/imagesaveoptions/pixelformat/
---
## ImageSaveOptions.PixelFormat property

Gets or sets the pixel format for the generated images.

```csharp
public ImagePixelFormat PixelFormat { get; set; }
```

## Remarks

This property has effect only when saving to raster image formats.

The default value is Format32BppArgb.

Pixel format of the output image may differ from the set value because of work of GDI+.

## Examples

Shows how to select a bit-per-pixel rate with which to render a document to an image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// When we save the document as an image, we can pass a SaveOptions object to
// select a pixel format for the image that the saving operation will generate.
// Various bit per pixel rates will affect the quality and file size of the generated image.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

// We can clone ImageSaveOptions instances.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### See Also

* enum [ImagePixelFormat](../../imagepixelformat/)
* class [ImageSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
