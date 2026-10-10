---
title: PdfSaveOptions.compliance property
linktitle: compliance property
articleTitle: compliance property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.compliance property. Specifies the PDF standards compliance level for output documents."
type: docs
weight: 50
url: /ru/python-net/aspose.words.saving/pdfsaveoptions/compliance/
---

## PdfSaveOptions.compliance property

Specifies the PDF standards compliance level for output documents.


```python
@property
def compliance(self) -> aspose.words.saving.PdfCompliance:
    ...

@compliance.setter
def compliance(self, value: aspose.words.saving.PdfCompliance):
    ...

```

### Remarks

Default is [PdfCompliance.PDF17](../../pdfcompliance/#PDF17).




### Examples

Shows how to set the PDF standards compliance level of saved PDF documents.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
# Обратите внимание, что некоторые PdfSaveOptions запрещены при сохранении в один из стандартов и автоматически исправляются.
# Используйте IWarningCallback, чтобы узнать, какие параметры автоматически исправлены.
save_options = aw.saving.PdfSaveOptions()
# Установите свойство "Compliance" в "PdfCompliance.PdfA1b", чтобы соответствовать стандарту "PDF/A-1b",
# что направлено на сохранение визуального вида документа при конвертации Aspose.Words в PDF.
# Установите свойство "Compliance" в "PdfCompliance.Pdf17", чтобы соответствовать стандарту "1.7".
# Установите свойство "Compliance" в "PdfCompliance.PdfA1a", чтобы соответствовать стандарту "PDF/A-1a",
# которая соответствует "PDF/A-1b" и сохраняет структуру оригинального документа.
# Установите свойство "Compliance" в "PdfCompliance.PdfUa1", чтобы соответствовать стандарту "PDF/UA-1" (ISO 14289-1),
# которая направлена на определение представления электронных документов в PDF, позволяющих файлу быть доступным.
# Установите свойство "Compliance" в "PdfCompliance.Pdf20", чтобы соответствовать стандарту "PDF 2.0" (ISO 32000-2).
# Установите свойство "Compliance" в "PdfCompliance.PdfA4", чтобы соответствовать стандарту "PDF/A-4" (ISO 19004:2020),
# которая сохраняет статический визуальный вид документа со временем.
# Установите свойство "Compliance" в "PdfCompliance.PdfA4Ua2", чтобы соответствовать обоим PDF/A-4 (ISO 19005-4:2020)
# и PDF/UA-2 (ISO 14289-2:2024) стандартам.
# Установите свойство "Compliance" в "PdfCompliance.PdfUa2", чтобы соответствовать стандарту PDF/UA-2 (ISO 14289-2:2024).
# Это помогает сделать документы доступными для поиска, но может значительно увеличить размер уже больших документов.
save_options.compliance = pdf_compliance
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.Compliance.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

