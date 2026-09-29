---
title: PdfSaveOptions.additional_text_positioning property
linktitle: additional_text_positioning property
articleTitle: additional_text_positioning property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.additional_text_positioning property. A flag specifying whether to write additional text positioning operators or not."
type: docs
weight: 20
url: /ru/python-net/aspose.words.saving/pdfsaveoptions/additional_text_positioning/
---

## PdfSaveOptions.additional_text_positioning property

A flag specifying whether to write additional text positioning operators or not.


```python
@property
def additional_text_positioning(self) -> bool:
    ...

@additional_text_positioning.setter
def additional_text_positioning(self, value: bool):
    ...

```

### Remarks

If ``True``, additional text positioning operators are written to the output PDF. This may help to overcome
issues with inaccurate text positioning with some printers. The downside is the increased PDF document size.


The default value is ``False``.




### Examples

Show how to write additional text positioning operators.

```python
doc = aw.Document(file_name=MY_DIR + 'Text positioning operators.docx')
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
save_options = aw.saving.PdfSaveOptions()
save_options.text_compression = aw.saving.PdfTextCompression.NONE
# Установите свойство "AdditionalTextPositioning" в "true", чтобы попытаться исправить некорректное
# позиционирование элементов в выходном PDF, если оно есть, ценой увеличения размера файла.
# Установите свойство "AdditionalTextPositioning" в "false", чтобы отрисовать документ как обычно.
save_options.additional_text_positioning = apply_additional_text_positioning
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.AdditionalTextPositioning.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

