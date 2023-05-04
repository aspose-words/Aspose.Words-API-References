---
title: PdfSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words for .NET
description: PdfSaveOptions JpegQuality property. Gets or sets a value determining the quality of the JPEG images inside PDF document in C#.
type: docs
weight: 220
url: /net/aspose.words.saving/pdfsaveoptions/jpegquality/
---
## PdfSaveOptions.JpegQuality property

Gets or sets a value determining the quality of the JPEG images inside PDF document.

```csharp
public int JpegQuality { get; set; }
```

## Remarks

The default value is 100.

This property is used in conjunction with the [`ImageCompression`](../imagecompression/) option.

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in PDF format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression. If quality is 100 and source image is JPEG, it means no compression - original bytes will be saved.

## Examples

Shows how to specify a compression type for all images in a document that we are converting to PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Set the "ImageCompression" property to "PdfImageCompression.Auto" to use the
// "ImageCompression" property to control the quality of the Jpeg images that end up in the output PDF.
// Set the "ImageCompression" property to "PdfImageCompression.Jpeg" to use the
// "ImageCompression" property to control the quality of all images that end up in the output PDF.
pdfSaveOptions.ImageCompression = pdfImageCompression;

// Set the "JpegQuality" property to "10" to strengthen compression at the cost of image quality.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../pdfsaveoptions/)
* assembly [Aspose.Words](../../../)
