---
title: PdfImageCompression Enum
linktitle: PdfImageCompression
articleTitle: PdfImageCompression
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Saving.PdfImageCompression enum. Specifies the type of compression applied to images in the PDF file in C#.
type: docs
weight: 5400
url: /net/aspose.words.saving/pdfimagecompression/
---
## PdfImageCompression enumeration

Specifies the type of compression applied to images in the PDF file.

```csharp
public enum PdfImageCompression
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Auto | `0` | Automatically selects the most appropriate compression for each image. |
| Jpeg | `1` | Jpeg compression. Does not support transparency. |

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

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
