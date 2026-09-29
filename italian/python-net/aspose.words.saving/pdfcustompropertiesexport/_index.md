---
title: PdfCustomPropertiesExport enumeration
linktitle: PdfCustomPropertiesExport enumeration
articleTitle: PdfCustomPropertiesExport enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfCustomPropertiesExport enumeration. Specifies the way [Document.custom_document_properties](../../aspose.words/document/custom_document_properties/) are exported to PDF file."
type: docs
weight: 640
url: /it/python-net/aspose.words.saving/pdfcustompropertiesexport/
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

* module [aspose.words.saving](../)

