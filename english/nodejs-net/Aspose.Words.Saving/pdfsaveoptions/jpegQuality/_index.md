---
title: PdfSaveOptions.jpegQuality property
linktitle: jpegQuality property
articleTitle: jpegQuality property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.jpegQuality property. Gets or sets a value determining the quality of the JPEG images inside PDF document."
type: docs
weight: 220
url: /nodejs-net/Aspose.Words.Saving/pdfsaveoptions/jpegQuality/
---

## PdfSaveOptions.jpegQuality property

Gets or sets a value determining the quality of the JPEG images inside PDF document.


```js
get jpegQuality(): number
```

### Remarks

The default value is 100.

This property is used in conjunction with the [PdfSaveOptions.imageCompression](../imageCompression/) option.

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in PDF format.
The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100
means best quality but minimum compression.
If quality is 100 and source image is JPEG, it means no compression - original bytes will be saved.




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

