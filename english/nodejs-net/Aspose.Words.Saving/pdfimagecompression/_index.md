---
title: PdfImageCompression enumeration
linktitle: PdfImageCompression enumeration
articleTitle: PdfImageCompression enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.PdfImageCompression enumeration. Specifies the type of compression applied to images in the PDF file."
type: docs
weight: 680
url: /nodejs-net/Aspose.Words.Saving/pdfimagecompression/
---

## PdfImageCompression enumeration

Specifies the type of compression applied to images in the PDF file.


### Members

| Name | Description |
| --- | --- |
| Auto | Automatically selects the most appropriate compression for each image. |
| Jpeg | Jpeg compression. Does not support transparency. |

### Examples

Shows how to specify a compression type for all images in a document that we are converting to PDF.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Jpeg image:");
builder.insertImage(base.imageDir + "Logo.jpg");
builder.insertParagraph();
builder.writeln("Png image:");
builder.insertImage(base.imageDir + "Transparent background logo.png");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let pdfSaveOptions = new aw.Saving.PdfSaveOptions();
// Set the "ImageCompression" property to "PdfImageCompression.Auto" to use the
// "ImageCompression" property to control the quality of the Jpeg images that end up in the output PDF.
// Set the "ImageCompression" property to "PdfImageCompression.Jpeg" to use the
// "ImageCompression" property to control the quality of all images that end up in the output PDF.
pdfSaveOptions.imageCompression = pdfImageCompression;
// Set the "JpegQuality" property to "10" to strengthen compression at the cost of image quality.
pdfSaveOptions.jpegQuality = 10;

doc.save(base.artifactsDir + "PdfSaveOptions.imageCompression.pdf", pdfSaveOptions);
```

### See Also

* module [Aspose.Words.Saving](../)

