---
title: PdfCustomPropertiesExport enumeration
linktitle: PdfCustomPropertiesExport enumeration
articleTitle: PdfCustomPropertiesExport enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfCustomPropertiesExport enumeration. Specifies the way [Document.custom_document_properties](../../aspose.words/document/custom_document_properties/) are exported to PDF file."
type: docs
weight: 640
url: /es/python-net/aspose.words.saving/pdfcustompropertiesexport/
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
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
options = aw.saving.PdfSaveOptions()
# Establezca la propiedad "CustomPropertiesExport" a "PdfCustomPropertiesExport.None" para descartar
# propiedades personalizadas del documento al guardar el documento en .PDF.
# Establezca la propiedad "CustomPropertiesExport" a "PdfCustomPropertiesExport.Standard"
# para preservar propiedades personalizadas dentro del documento PDF de salida.
# Establezca la propiedad "CustomPropertiesExport" a "PdfCustomPropertiesExport.Metadata"
# para preservar propiedades personalizadas en un paquete XMP.
options.custom_properties_export = pdf_custom_properties_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.CustomPropertiesExport.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

