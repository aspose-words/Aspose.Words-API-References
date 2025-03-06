---
title: PdfSaveOptions.CustomPropertiesExport
linktitle: CustomPropertiesExport
articleTitle: CustomPropertiesExport
second_title: Aspose.Words for .NET
description: Discover how the PdfSaveOptions CustomPropertiesExport property enhances your PDF exports by controlling CustomDocumentProperties for optimal results.
type: docs
weight: 70
url: /net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

Gets or sets a value determining the way [`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/) are exported to PDF file.

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

## Remarks

Default value is None.

Metadata value is not supported when saving to PDF/A. Standard will be used instead for PDF/A-1 and PDF/A-2 and None for PDF/A-4.

Standard value is not supported when saving to PDF 2.0. Metadata will be used instead.

## Examples

Shows how to export custom properties while converting a document to PDF.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.None" to discard
// custom document properties as we save the document to .PDF.
// Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.Standard"
// to preserve custom properties within the output PDF document.
// Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.Metadata"
// to preserve custom properties in an XMP packet.
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### See Also

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
