---
title: PdfSaveOptions.custom_properties_export property
linktitle: custom_properties_export property
articleTitle: custom_properties_export property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.custom_properties_export property. Gets or sets a value determining the way [Document.custom_document_properties](../../../aspose.words/document/custom_document_properties/) are exported to PDF file."
type: docs
weight: 70
url: /sv/python-net/aspose.words.saving/pdfsaveoptions/custom_properties_export/
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
doc.custom_document_properties.add(name='Company', value='My value')
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
options = aw.saving.PdfSaveOptions()
# Ställ in egenskapen "CustomPropertiesExport" till "PdfCustomPropertiesExport.None" för att förkasta
# anpassade dokumentegenskaper när vi sparar dokumentet till .PDF.
# Ställ in egenskapen "CustomPropertiesExport" till "PdfCustomPropertiesExport.Standard"
# för att bevara anpassade egenskaper i den genererade PDF-dokumentet.
# Ställ in egenskapen "CustomPropertiesExport" till "PdfCustomPropertiesExport.Metadata"
# för att bevara anpassade egenskaper i ett XMP-paket.
options.custom_properties_export = pdf_custom_properties_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.CustomPropertiesExport.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

