---
title: ImageSaveOptions.ImageSize
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words for .NET
description: Discover the ImageSize property of ImageSaveOptions to easily manage and customize image dimensions in pixels for optimal results.
type: docs
weight: 70
url: /net/aspose.words.saving/imagesaveoptions/imagesize/
---
## ImageSaveOptions.ImageSize property

Gets or sets the size of a generated image in pixels.

```csharp
public Size ImageSize { get; set; }
```

## Remarks

This property has effect only when saving to raster image formats.

The default value is (0 x 0), which means that the size of the generated image will be calculated according to the size of the image in points, the specified resolution and scale.

## Examples

Shows how to render every page of a document to a separate TIFF image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Set the "PageSet" property to the number of the first page from
    // which to start rendering the document from.
    options.PageSet = new PageSet(i);
    // Export page at 2325x5325 pixels and 600 dpi.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

### See Also

* class [ImageSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
