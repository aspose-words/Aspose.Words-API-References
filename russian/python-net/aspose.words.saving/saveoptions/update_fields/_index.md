---
title: SaveOptions.update_fields property
linktitle: update_fields property
articleTitle: update_fields property
second_title: Aspose.Words for Python
description: "SaveOptions.update_fields property. Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format"
type: docs
weight: 150
url: /ru/python-net/aspose.words.saving/saveoptions/update_fields/
---

## SaveOptions.update_fields property

Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format.
Default value for this property is ``True``.



```python
@property
def update_fields(self) -> bool:
    ...

@update_fields.setter
def update_fields(self, value: bool):
    ...

```

### Remarks

Allows to specify whether to mimic or not MS Word behavior.


### Examples

Shows how to update all the fields in a document immediately before saving it to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставить текст с полями PAGE и NUMPAGES. Эти поля не отображают правильное значение в реальном времени.
# Нам потребуется вручную обновлять их, используя методы обновления, такие как "Field.Update()" и "Document.UpdateFields()"
# каждый раз, когда нам нужно, чтобы они отображали точные значения.
builder.write('Page ')
builder.insert_field(field_code='PAGE', field_value='')
builder.write(' of ')
builder.insert_field(field_code='NUMPAGES', field_value='')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Hello World!')
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
options = aw.saving.PdfSaveOptions()
# Установите свойство "UpdateFields" в "false", чтобы не обновлять все поля в документе непосредственно перед операцией сохранения.
# Это предпочтительный вариант, если мы знаем, что все наши поля будут актуальны перед сохранением.
# Установите свойство "UpdateFields" в "true", чтобы пройти по всему документу
# полям и обновить их перед сохранением в PDF. Это гарантирует, что все поля будут отображать
# наиболее точные значения в PDF.
options.update_fields = update_fields
# Мы можем клонировать объекты PdfSaveOptions.
self.assertNotEqual(options, options.clone())
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.UpdateFields.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

