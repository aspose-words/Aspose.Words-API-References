---
title: PdfCustomPropertiesExport enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the way [Document.custom_document_properties](../../aspose.words/document/custom_document_properties/) are exported to PDF file."
type: docs
weight: 550
url: /python-net/aspose.words.saving/pdfcustompropertiesexport/
---

## PdfCustomPropertiesExport enumeration

Specifies the way [Document.custom_document_properties](../../aspose.words/document/custom_document_properties/) are exported to PDF file.



### Members

| Name | Description |
| --- | --- |
| NONE | No custom properties are exported. |
| STANDARD | Custom properties are exported as entries in /Info dictionary. Custom properties with the following names are not exported: "Title", "Author", "Subject", "Keywords", "Creator", "Producer", "CreationDate", "ModDate", "Trapped". |
| METADATA | Custom properties are Metadata. |

### Examples

Shows how to export custom properties while converting a document to PDF.

```python
doc = aw.Document()

doc.custom_document_properties.add("Company", "My value")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()

# Set the "custom_properties_export" property to "PdfCustomPropertiesExport.NONE" to discard
# custom document properties as we save the document to .PDF.
# Set the "custom_properties_export" property to "PdfCustomPropertiesExport.STANDARD"
# to preserve custom properties within the output PDF document.
# Set the "custom_properties_export" property to "PdfCustomPropertiesExport.METADATA"
# to preserve custom properties in an XMP packet.
options.custom_properties_export = pdf_custom_properties_export_mode

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.custom_properties_export.pdf", options)
```

### See Also

* module [aspose.words.saving](../)

