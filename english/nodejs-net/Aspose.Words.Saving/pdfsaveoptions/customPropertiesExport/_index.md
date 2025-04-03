---
title: PdfSaveOptions.customPropertiesExport property
linktitle: customPropertiesExport property
articleTitle: customPropertiesExport property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.customPropertiesExport property. Gets or sets a value determining the way [Document.customDocumentProperties](../../../aspose.words/document/customDocumentProperties/) are exported to PDF file."
type: docs
weight: 70
url: /nodejs-net/Aspose.Words.Saving/pdfsaveoptions/customPropertiesExport/
---

## PdfSaveOptions.customPropertiesExport property

Gets or sets a value determining the way [Document.customDocumentProperties](../../../aspose.words/document/customDocumentProperties/) are exported to PDF file.



```js
get customPropertiesExport(): Aspose.Words.Saving.PdfCustomPropertiesExport
```

### Remarks

Default value is [PdfCustomPropertiesExport.None](../../pdfcustompropertiesexport/#None).

[PdfCustomPropertiesExport.Metadata](../../pdfcustompropertiesexport/#Metadata) value is not supported when saving to PDF/A.
[PdfCustomPropertiesExport.Standard](../../pdfcustompropertiesexport/#Standard) will be used instead for PDF/A-1 and PDF/A-2 and
[PdfCustomPropertiesExport.None](../../pdfcustompropertiesexport/#None) for PDF/A-4.

[PdfCustomPropertiesExport.Standard](../../pdfcustompropertiesexport/#Standard) value is not supported when saving to PDF 2.0.
[PdfCustomPropertiesExport.Metadata](../../pdfcustompropertiesexport/#Metadata) will be used instead.




### Examples

Shows how to export custom properties while converting a document to PDF.

```js
let doc = new aw.Document();

doc.customDocumentProperties.add("Company", "My value");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.None" to discard
// custom document properties as we save the document to .PDF.
// Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.Standard"
// to preserve custom properties within the output PDF document.
// Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.Metadata"
// to preserve custom properties in an XMP packet.
options.customPropertiesExport = pdfCustomPropertiesExportMode;

doc.save(base.artifactsDir + "PdfSaveOptions.customPropertiesExport.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

