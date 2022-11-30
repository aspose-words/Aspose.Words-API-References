---
title: get_CustomPropertiesExport
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining the way CustomDocumentProperties are exported to PDF file.
type: docs
weight: 79
url: /cpp/aspose.words.saving/pdfsaveoptions/get_custompropertiesexport/
---
## PdfSaveOptions::get_CustomPropertiesExport method


Gets or sets a value determining the way [CustomDocumentProperties](../../../aspose.words/document/get_customdocumentproperties/) are exported to PDF file.

```cpp
Aspose::Words::Saving::PdfCustomPropertiesExport Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport() const
```

## Remarks


Default value is [None](../../pdfcustompropertiesexport/).

[Metadata](../../pdfcustompropertiesexport/) value is not supported when saving to PDF/A. [Standard](../../pdfcustompropertiesexport/) will be used instead for PDF/A-1 and PDF/A-2 and [None](../../pdfcustompropertiesexport/) for PDF/A-4.

[Standard](../../pdfcustompropertiesexport/) value is not supported when saving to PDF 2.0. [Metadata](../../pdfcustompropertiesexport/) will be used instead.

## Examples



Shows how to export custom properties while converting a document to PDF. 
```cpp
auto doc = MakeObject<Document>();

doc->get_CustomDocumentProperties()->Add(u"Company", String(u"My value"));

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.None" to discard
// custom document properties as we save the document to .PDF.
// Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.Standard"
// to preserve custom properties within the output PDF document.
// Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.Metadata"
// to preserve custom properties in an XMP packet.
options->set_CustomPropertiesExport(pdfCustomPropertiesExportMode);

doc->Save(ArtifactsDir + u"PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

## See Also

* Enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
