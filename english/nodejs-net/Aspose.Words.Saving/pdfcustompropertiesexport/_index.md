---
title: PdfCustomPropertiesExport enumeration
linktitle: PdfCustomPropertiesExport enumeration
articleTitle: PdfCustomPropertiesExport enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.PdfCustomPropertiesExport enumeration. Specifies the way [Document.customDocumentProperties](../../aspose.words/document/customDocumentProperties/) are exported to PDF file."
type: docs
weight: 610
url: /nodejs-net/aspose.words.saving/pdfcustompropertiesexport/
---

## PdfCustomPropertiesExport enumeration

Specifies the way [Document.customDocumentProperties](../../aspose.words/document/customDocumentProperties/) are exported to PDF file.



### Members

| Name | Description |
| --- | --- |
| None | No custom properties are exported. |
| Standard | Custom properties are exported as entries in /Info dictionary. Custom properties with the following names are not exported: "Title", "Author", "Subject", "Keywords", "Creator", "Producer", "CreationDate", "ModDate", "Trapped". |
| Metadata | Custom properties are Metadata. |

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

* module [Aspose.Words.Saving](../)

