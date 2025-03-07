---
title: PdfSaveOptions.custom_properties_export property
linktitle: custom_properties_export property
articleTitle: custom_properties_export property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.custom_properties_export property. Gets or sets a value determining the way [Document.custom_document_properties](../../../aspose.words/document/custom_document_properties/) are exported to PDF file."
type: docs
weight: 70
url: /python-net/aspose.words.saving/pdfsaveoptions/custom_properties_export/
---

## PdfSaveOptions.custom_properties_export property

Gets or sets a value determining the way [Document.custom_document_properties](../../../aspose.words/document/custom_document_properties/) are exported to PDF file.



```python
@property
def custom_properties_export(self) -> aspose.words.saving.PdfCustomPropertiesExport:
    ...

@custom_properties_export.setter
def custom_properties_export(self, value: aspose.words.saving.PdfCustomPropertiesExport):
    ...

```

### Remarks

Default value is [PdfCustomPropertiesExport.NONE](../../pdfcustompropertiesexport/#NONE).

[PdfCustomPropertiesExport.METADATA](../../pdfcustompropertiesexport/#METADATA) value is not supported when saving to PDF/A.
[PdfCustomPropertiesExport.STANDARD](../../pdfcustompropertiesexport/#STANDARD) will be used instead for PDF/A-1 and PDF/A-2 and
[PdfCustomPropertiesExport.NONE](../../pdfcustompropertiesexport/#NONE) for PDF/A-4.

[PdfCustomPropertiesExport.STANDARD](../../pdfcustompropertiesexport/#STANDARD) value is not supported when saving to PDF 2.0.
[PdfCustomPropertiesExport.METADATA](../../pdfcustompropertiesexport/#METADATA) will be used instead.




### Examples

Shows how to export custom properties while converting a document to PDF.

```python
doc = aw.Document()
doc.custom_document_properties.add('Company', 'My value')
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
doc.save(ARTIFACTS_DIR + 'PdfSaveOptions.custom_properties_export.pdf', options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

