---
title: PdfSaveOptions.custom_properties_export property
linktitle: custom_properties_export property
articleTitle: custom_properties_export property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.custom_properties_export property. Gets or sets a value determining the way [Document.custom_document_properties](../../../aspose.words/document/custom_document_properties/) are exported to PDF file."
type: docs
weight: 70
url: /it/python-net/aspose.words.saving/pdfsaveoptions/custom_properties_export/
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
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
options = aw.saving.PdfSaveOptions()
# Imposta la proprietà "CustomPropertiesExport" a "PdfCustomPropertiesExport.None" per scartare
# le proprietà personalizzate del documento quando salviamo il documento in .PDF.
# Imposta la proprietà "CustomPropertiesExport" a "PdfCustomPropertiesExport.Standard"
# per preservare le proprietà personalizzate all'interno del documento PDF di output.
# Imposta la proprietà "CustomPropertiesExport" a "PdfCustomPropertiesExport.Metadata"
# per preservare le proprietà personalizzate in un pacchetto XMP.
options.custom_properties_export = pdf_custom_properties_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.CustomPropertiesExport.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

