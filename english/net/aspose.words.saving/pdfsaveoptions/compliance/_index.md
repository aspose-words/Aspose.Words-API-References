---
title: PdfSaveOptions.Compliance
linktitle: Compliance
second_title: Aspose.Words for .NET API Reference
description: PdfSaveOptions Compliance property. Specifies the PDF standards compliance level for output documents in C#.
type: docs
weight: 40
url: /net/aspose.words.saving/pdfsaveoptions/compliance/
---
## PdfSaveOptions.Compliance property

Specifies the PDF standards compliance level for output documents.

```csharp
public PdfCompliance Compliance { get; set; }
```

## Remarks

Default is Pdf17.

## Examples

Shows how to set the PDF standards compliance level of saved PDF documents.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
// Note that some PdfSaveOptions are prohibited when saving to one of the standards and automatically fixed.
// Use IWarningCallback to know which options are automatically fixed.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Set the "Compliance" property to "PdfCompliance.PdfA1b" to comply with the "PDF/A-1b" standard,
// which aims to preserve the visual appearance of the document as Aspose.Words convert it to PDF.
// Set the "Compliance" property to "PdfCompliance.Pdf17" to comply with the "1.7" standard.
// Set the "Compliance" property to "PdfCompliance.PdfA1a" to comply with the "PDF/A-1a" standard,
// which complies with "PDF/A-1b" as well as preserving the document structure of the original document.
// Set the "Compliance" property to "PdfCompliance.PdfUa1" to comply with the "PDF/UA-1" (ISO 14289-1) standard,
// which aims to define represent electronic documents in PDF that allow the file to be accessible.
// Set the "Compliance" property to "PdfCompliance.Pdf20" to comply with the "PDF 2.0" (ISO 32000-2) standard.
// Set the "Compliance" property to "PdfCompliance.PdfA4" to comply with the "PDF/A-4" (ISO 19004:2020) standard,
// which preserving document static visual appearance over time.
// This helps with making documents searchable but may significantly increase the size of already large documents.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### See Also

* enum [PdfCompliance](../../pdfcompliance/)
* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../pdfsaveoptions/)
* assembly [Aspose.Words](../../../)
