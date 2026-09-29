---
title: PdfCustomPropertiesExport enumeration
linktitle: PdfCustomPropertiesExport enumeration
articleTitle: PdfCustomPropertiesExport enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfCustomPropertiesExport enumeration. Specifies the way [Document.custom_document_properties](../../aspose.words/document/custom_document_properties/) are exported to PDF file."
type: docs
weight: 640
url: /ru/python-net/aspose.words.saving/pdfcustompropertiesexport/
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
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
options = aw.saving.PdfSaveOptions()
# Установите свойство "CustomPropertiesExport" в "PdfCustomPropertiesExport.None", чтобы отказаться от
# пользовательских свойств документа при сохранении его в .PDF.
# Установите свойство "CustomPropertiesExport" в "PdfCustomPropertiesExport.Standard"
# чтобы сохранить пользовательские свойства внутри выходного PDF‑документа.
# Установите свойство "CustomPropertiesExport" в значение "PdfCustomPropertiesExport.Metadata"
# чтобы сохранить пользовательские свойства в XMP‑пакете.
options.custom_properties_export = pdf_custom_properties_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.CustomPropertiesExport.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

