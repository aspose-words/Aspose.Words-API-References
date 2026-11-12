---
title: PdfCustomPropertiesExport enumeration
linktitle: PdfCustomPropertiesExport enumeration
articleTitle: PdfCustomPropertiesExport enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfCustomPropertiesExport enumeration. Specifies the way [Document.custom_document_properties](../../aspose.words/document/custom_document_properties/) are exported to PDF file."
type: docs
weight: 640
url: /tr/python-net/aspose.words.saving/pdfcustompropertiesexport/
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
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
options = aw.saving.PdfSaveOptions()
# \"CustomPropertiesExport\" özelliğini \"PdfCustomPropertiesExport.None\" olarak ayarlayın,
# belgeyi .PDF olarak kaydederken özel belge özelliklerini göz ardı etmek için.
# \"CustomPropertiesExport\" özelliğini \"PdfCustomPropertiesExport.Standard\" olarak ayarlayın
# çıktı PDF belgesi içinde özel özellikleri korumak için.
# Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.Metadata"
# XMP paketinde özel özellikleri korumak için.
options.custom_properties_export = pdf_custom_properties_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.CustomPropertiesExport.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

