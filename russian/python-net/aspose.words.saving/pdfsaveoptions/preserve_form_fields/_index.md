---
title: PdfSaveOptions.preserve_form_fields property
linktitle: preserve_form_fields property
articleTitle: preserve_form_fields property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.preserve_form_fields property. Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text"
type: docs
weight: 300
url: /ru/python-net/aspose.words.saving/pdfsaveoptions/preserve_form_fields/
---

## PdfSaveOptions.preserve_form_fields property

Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text.
Default is ``False``.



```python
@property
def preserve_form_fields(self) -> bool:
    ...

@preserve_form_fields.setter
def preserve_form_fields(self, value: bool):
    ...

```

### Remarks

Microsoft Word form fields include text input, drop down and check box controls.

When set to ``False``, these fields will be exported as text to PDF. When set to ``True``,
these fields will be exported as PDF form fields.

When exporting form fields to PDF as form fields, some formatting loss might occur because PDF form
fields do not support all features of Microsoft Word form fields.

Also, the output size depends on the content size because editable forms in Microsoft Word are
inline objects.




### Examples

Shows how to save a document to the PDF format using the Save method and the PdfSaveOptions class.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Please select a fruit: ')
# Вставьте комбобокс, который позволит пользователю выбрать вариант из набора строк.
builder.insert_combo_box('MyComboBox', ['Apple', 'Banana', 'Cherry'], 0)
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
pdf_options = aw.saving.PdfSaveOptions()
# Установите свойство "PreserveFormFields" в значение "true", чтобы сохранять поля формы как интерактивные объекты в выходном PDF.
# Установите свойство "PreserveFormFields" в значение "false", чтобы заморозить все поля формы в документе на
# их текущих значениях и отобразить их как обычный текст в выходном PDF.
pdf_options.preserve_form_fields = preserve_form_fields
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PreserveFormFields.pdf', save_options=pdf_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

