---
title: PdfSaveOptions.compliance property
linktitle: compliance property
articleTitle: compliance property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.compliance property. Specifies the PDF standards compliance level for output documents."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words.Saving/pdfsaveoptions/compliance/
---

## PdfSaveOptions.compliance property

Specifies the PDF standards compliance level for output documents.


```js
get compliance(): Aspose.Words.Saving.PdfCompliance
```

### Remarks

Default is [PdfCompliance.Pdf17](../../pdfcompliance/#Pdf17).




### Examples

Shows how to set the PDF standards compliance level of saved PDF documents.

```js
let doc = new aw.Document(base.myDir + "Images.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
// Note that some PdfSaveOptions are prohibited when saving to one of the standards and automatically fixed.
// Use IWarningCallback to know which options are automatically fixed.
let saveOptions = new aw.Saving.PdfSaveOptions();

// Set the "Compliance" property to "PdfCompliance.PdfA1b" to comply with the "PDF/A-1b" standard,
// which aims to preserve the visual appearance of the document as Aspose.words convert it to PDF.
// Set the "Compliance" property to "PdfCompliance.Pdf17" to comply with the "1.7" standard.
// Set the "Compliance" property to "PdfCompliance.PdfA1a" to comply with the "PDF/A-1a" standard,
// which complies with "PDF/A-1b" as well as preserving the document structure of the original document.
// Set the "Compliance" property to "PdfCompliance.PdfUa1" to comply with the "PDF/UA-1" (ISO 14289-1) standard,
// which aims to define represent electronic documents in PDF that allow the file to be accessible.
// Set the "Compliance" property to "PdfCompliance.Pdf20" to comply with the "PDF 2.0" (ISO 32000-2) standard.
// Set the "Compliance" property to "PdfCompliance.PdfA4" to comply with the "PDF/A-4" (ISO 19004:2020) standard,
// which preserving document static visual appearance over time.
// Set the "Compliance" property to "PdfCompliance.PdfA4Ua2" to comply with both PDF/A-4 (ISO 19005-4:2020)
// and PDF/UA-2 (ISO 14289-2:2024) standards.
// Set the "Compliance" property to "PdfCompliance.PdfUa2" to comply with the PDF/UA-2 (ISO 14289-2:2024) standard.
// This helps with making documents searchable but may significantly increase the size of already large documents.
saveOptions.compliance = pdfCompliance;

doc.save(base.artifactsDir + "PdfSaveOptions.compliance.pdf", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

