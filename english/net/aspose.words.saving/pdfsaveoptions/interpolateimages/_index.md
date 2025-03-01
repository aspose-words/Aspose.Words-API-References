---
title: PdfSaveOptions.InterpolateImages
linktitle: InterpolateImages
articleTitle: InterpolateImages
second_title: Aspose.Words for .NET
description: Discover PdfSaveOptions' InterpolateImages property, a key feature that enhances image quality in your documents. Optimize your PDFs effortlessly!
type: docs
weight: 210
url: /net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

A flag indicating whether image interpolation shall be performed by a conforming reader. When `false` is specified, the flag is not written to the output document and the default behaviour of reader is used instead.

```csharp
public bool InterpolateImages { get; set; }
```

## Remarks

When the resolution of a source image is significantly lower than that of the output device, each source sample covers many device pixels. As a result, images can appear jaggy or blocky. These visual artifacts can be reduced by applying an image interpolation algorithm during rendering. Instead of painting all pixels covered by a source sample with the same color, image interpolation attempts to produce a smooth transition between adjacent sample values.

A conforming Reader may choose to not implement this feature of PDF, or may use any specific implementation of interpolation that it wishes.

The default value is `false`.

Interpolation flag is prohibited by PDF/A compliance. `false` value will be used automatically when saving to PDF/A.

## Examples

Shows how to perform interpolation on images while saving a document to PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Set the "InterpolateImages" property to "true" to get the reader that opens this document to interpolate images.
// Their resolution should be lower than that of the device that is displaying the document.
// Set the "InterpolateImages" property to "false" to make it so that the reader does not apply any interpolation.
saveOptions.InterpolateImages = interpolateImages;

// When we open this document with a reader such as Adobe Acrobat, we will need to zoom in on the image
// to see the interpolation effect if we saved the document with it enabled.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
