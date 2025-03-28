---
title: PdfSaveOptions.ImageCompression
linktitle: ImageCompression
articleTitle: ImageCompression
second_title: Aspose.Words for .NET
description: Optimize your PDF with PdfSaveOptions' ImageCompression property, allowing you to choose the best compression type for vibrant, high-quality images.
type: docs
weight: 200
url: /net/aspose.words.saving/pdfsaveoptions/imagecompression/
---
## PdfSaveOptions.ImageCompression property

Specifies compression type to be used for all images in the document.

```csharp
public PdfImageCompression ImageCompression { get; set; }
```

## Remarks

Default is Auto.

Using Jpeg lets you control the quality of images in the output document through the [`JpegQuality`](../jpegquality/) property.

Using Jpeg provides the fastest conversion speed when compared to the performance of other compression types, but in this case, there is lossy JPEG compression.

Using Auto lets to control the quality of Jpeg in the output document through the [`JpegQuality`](../jpegquality/) property, but for other formats, raw pixel data is extracted and saved with Flate compression. This case is slower than Jpeg conversion but lossless.

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

* enum [PdfImageCompression](../../pdfimagecompression/)
* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
