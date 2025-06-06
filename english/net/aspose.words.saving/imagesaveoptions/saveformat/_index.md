---
title: ImageSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words for .NET
description: Discover the ImageSaveOptions SaveFormat property to effortlessly save documents in formats like TIFF, PNG, JPEG, and more. Enhance your workflow today!
type: docs
weight: 150
url: /net/aspose.words.saving/imagesaveoptions/saveformat/
---
## ImageSaveOptions.SaveFormat property

Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. Can be a raster Tiff, Png, Bmp, Jpeg or vector Emf, Eps, WebP, Svg.

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Remarks

The number of other options depends on the selected format.

Also, it is possible to save to SVG both via [`ImageSaveOptions`](../) and via [`SvgSaveOptions`](../../svgsaveoptions/).

## Examples

Shows how to edit the image while Aspose.Words converts a document to one.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// When we save the document as an image, we can pass a SaveOptions object to
// edit the image while the saving operation renders it.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // We can adjust these properties to change the image's brightness and contrast.
    // Both are on a 0-1 scale and are at 0.5 by default.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // We can adjust horizontal and vertical resolution with these properties.
    // This will affect the dimensions of the image.
    // The default value for these properties is 96.0, for a resolution of 96dpi.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // We can scale the image using this property. The default value is 1.0, for scaling of 100%.
    // We can use this property to negate any changes in image dimensions that changing the resolution would cause.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
