---
title: ImageSaveOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words for .NET
description: Optimize your images with ImageSaveOptions! Control horizontal and vertical resolution in DPI for stunning quality and clarity. Enhance your visuals today!
type: docs
weight: 140
url: /net/aspose.words.saving/imagesaveoptions/resolution/
---
## ImageSaveOptions.Resolution property

Sets both horizontal and vertical resolution for the generated images, in dots per inch.

```csharp
public float Resolution { set; }
```

## Remarks

This property has effect only when saving to raster image formats.

## Examples

Shows how to specify a resolution while rendering a document to PNG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

// Set the "Resolution" property to "72" to render the document in 72dpi.
options.Resolution = 72;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

// Set the "Resolution" property to "300" to render the document in 300dpi.
options.Resolution = 300;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);
```

### See Also

* class [ImageSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
