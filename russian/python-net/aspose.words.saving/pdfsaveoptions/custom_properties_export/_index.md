---
title: PdfSaveOptions.custom_properties_export property
linktitle: custom_properties_export property
articleTitle: custom_properties_export property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.custom_properties_export property. Gets or sets a value determining the way [Document.custom_document_properties](../../../aspose.words/document/custom_document_properties/) are exported to PDF file."
type: docs
weight: 70
url: /ru/python-net/aspose.words.saving/pdfsaveoptions/custom_properties_export/
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

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

