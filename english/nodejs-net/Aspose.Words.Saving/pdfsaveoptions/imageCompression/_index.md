---
title: PdfSaveOptions.imageCompression property
linktitle: imageCompression property
articleTitle: imageCompression property
second_title: Aspose.Words for Node.js
description: "PdfSaveOptions.imageCompression property. Specifies compression type to be used for all images in the document."
type: docs
weight: 200
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/imageCompression/
---

## PdfSaveOptions.imageCompression property

Specifies compression type to be used for all images in the document.


```js
get imageCompression(): Aspose.Words.Saving.PdfImageCompression
```

### Remarks

Default is [PdfImageCompression.Auto](../../pdfimagecompression/#Auto).

Using [PdfImageCompression.Jpeg](../../pdfimagecompression/#Jpeg) lets you control the quality of images in the output document through the [PdfSaveOptions.jpegQuality](../jpegQuality/) property.

Using [PdfImageCompression.Jpeg](../../pdfimagecompression/#Jpeg) provides the fastest conversion speed when compared to the performance of other compression types,
but in this case, there is lossy JPEG compression.

Using [PdfImageCompression.Auto](../../pdfimagecompression/#Auto) lets to control the quality of Jpeg in the output document through the [PdfSaveOptions.jpegQuality](../jpegQuality/) property,
but for other formats, raw pixel data is extracted and saved with Flate compression.
This case is slower than Jpeg conversion but lossless.




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

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

