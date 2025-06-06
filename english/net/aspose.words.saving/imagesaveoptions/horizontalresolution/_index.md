---
title: ImageSaveOptions.HorizontalResolution
linktitle: HorizontalResolution
articleTitle: HorizontalResolution
second_title: Aspose.Words for .NET
description: Discover the ImageSaveOptions HorizontalResolution property to easily adjust image quality in DPI for optimal clarity and detail in your projects.
type: docs
weight: 30
url: /net/aspose.words.saving/imagesaveoptions/horizontalresolution/
---
## ImageSaveOptions.HorizontalResolution property

Gets or sets the horizontal resolution for the generated images, in dots per inch.

```csharp
public float HorizontalResolution { get; set; }
```

## Remarks

This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.

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

* class [ImageSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
