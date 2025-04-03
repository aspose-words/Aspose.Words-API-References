---
title: PdfSaveOptions.imageColorSpaceExportMode property
linktitle: imageColorSpaceExportMode property
articleTitle: imageColorSpaceExportMode property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.imageColorSpaceExportMode property. Specifies how the color space will be selected for the images in PDF document."
type: docs
weight: 190
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/imageColorSpaceExportMode/
---

## PdfSaveOptions.imageColorSpaceExportMode property

Specifies how the color space will be selected for the images in PDF document.


```js
get imageColorSpaceExportMode(): Aspose.Words.Saving.PdfImageColorSpaceExportMode
```

### Remarks

The default value is [PdfImageColorSpaceExportMode.Auto](../../pdfimagecolorspaceexportmode/#Auto).


If [PdfImageColorSpaceExportMode.SimpleCmyk](../../pdfimagecolorspaceexportmode/#SimpleCmyk) value is specified,
[PdfSaveOptions.imageCompression](../imageCompression/) option is ignored and
Flate compression is used for all images in the document.


[PdfImageColorSpaceExportMode.SimpleCmyk](../../pdfimagecolorspaceexportmode/#SimpleCmyk) value is not supported when saving to PDF/A.
[PdfImageColorSpaceExportMode.Auto](../../pdfimagecolorspaceexportmode/#Auto) value will be used instead.




### Examples

Shows how to set a different color space for images in a document as we export it to PDF.

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

// Set the "ImageColorSpaceExportMode" property to "PdfImageColorSpaceExportMode.Auto" to get Aspose.words to
// automatically select the color space for images in the document that it converts to PDF.
// In most cases, the color space will be RGB.
// Set the "ImageColorSpaceExportMode" property to "PdfImageColorSpaceExportMode.SimpleCmyk"
// to use the CMYK color space for all images in the saved PDF.
// Aspose.words will also apply Flate compression to all images and ignore the "ImageCompression" property's value.
pdfSaveOptions.imageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.save(base.artifactsDir + "PdfSaveOptions.imageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

