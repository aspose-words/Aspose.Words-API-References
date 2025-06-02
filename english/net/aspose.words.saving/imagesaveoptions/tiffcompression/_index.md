---
title: ImageSaveOptions.TiffCompression
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words for .NET
description: Optimize your TIFF images with the ImageSaveOptions TiffCompression property, allowing you to choose the best compression method for quality results.
type: docs
weight: 190
url: /net/aspose.words.saving/imagesaveoptions/tiffcompression/
---
## ImageSaveOptions.TiffCompression property

Gets or sets the type of compression to apply when saving generated images to the TIFF format.

```csharp
public TiffCompression TiffCompression { get; set; }
```

## Remarks

Has effect only when saving to TIFF.

The default value is Lzw.

## Examples

Shows how to select the compression scheme to apply to a document that we convert into a TIFF image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
// Set the "TiffCompression" property to "TiffCompression.None" to apply no compression while saving,
// which may result in a very large output file.
// Set the "TiffCompression" property to "TiffCompression.Rle" to apply RLE compression
// Set the "TiffCompression" property to "TiffCompression.Lzw" to apply LZW compression.
// Set the "TiffCompression" property to "TiffCompression.Ccitt3" to apply CCITT3 compression.
// Set the "TiffCompression" property to "TiffCompression.Ccitt4" to apply CCITT4 compression.
options.TiffCompression = tiffCompression;

doc.Save(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff", options);
```

### See Also

* enum [TiffCompression](../../tiffcompression/)
* class [ImageSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
