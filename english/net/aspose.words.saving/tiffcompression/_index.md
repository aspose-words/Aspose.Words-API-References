---
title: TiffCompression Enum
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.TiffCompression enum for optimal TIFF file saving. Choose the best compression type for high-quality page images effortlessly.
type: docs
weight: 6490
url: /net/aspose.words.saving/tiffcompression/
---
## TiffCompression enumeration

Specifies what type of compression to apply when saving page images into a TIFF file.

```csharp
public enum TiffCompression
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | Specifies no compression. |
| Rle | `1` | Specifies the RLE compression scheme. |
| Lzw | `2` | Specifies the LZW compression scheme. In Java emulated by Deflate (Zip) compression. |
| Ccitt3 | `3` | Specifies the CCITT3 compression scheme. |
| Ccitt4 | `4` | Specifies the CCITT4 compression scheme. |

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

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
