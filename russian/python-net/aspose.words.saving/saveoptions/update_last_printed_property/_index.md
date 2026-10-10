---
title: SaveOptions.update_last_printed_property property
linktitle: update_last_printed_property property
articleTitle: update_last_printed_property property
second_title: Aspose.Words for Python
description: "SaveOptions.update_last_printed_property property. Gets or sets a value determining whether the [BuiltInDocumentProperties.last_printed](../../../aspose.words.properties/builtindocumentproperties/last_printed/) property is updated before saving."
type: docs
weight: 160
url: /ru/python-net/aspose.words.saving/saveoptions/update_last_printed_property/
---

## SaveOptions.update_last_printed_property property

Gets or sets a value determining whether the [BuiltInDocumentProperties.last_printed](../../../aspose.words.properties/builtindocumentproperties/last_printed/) property is updated before saving.



```python
@property
def update_last_printed_property(self) -> bool:
    ...

@update_last_printed_property.setter
def update_last_printed_property(self, value: bool):
    ...

```

### Examples

Shows how to update a document's "Last printed" property when saving.

```python
doc = aw.Document()
last_printed = datetime.datetime(2019, 12, 20)
doc.built_in_document_properties.last_printed = last_printed
# Этот флаг определяет, обновляется ли дата последней печати, которая является встроенным свойством.
# Если да, то дата последней операции сохранения документа
# с переданным в качестве параметра объектом SaveOptions используется в качестве даты печати.
save_options = aw.saving.DocSaveOptions()
save_options.update_last_printed_property = is_update_last_printed_property
# В Microsoft Word 2003 это свойство можно найти через Файл -> Свойства -> Статистика -> Печать.
# Оно также может быть отображено в теле документа с помощью поля PRINTDATE.
doc.save(file_name=ARTIFACTS_DIR + 'DocSaveOptions.UpdateLastPrintedProperty.doc', save_options=save_options)
# Откройте сохранённый документ, затем проверьте значение свойства.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.UpdateLastPrintedProperty.doc')
if is_update_last_printed_property:
    self.assertNotEqual(last_printed, doc.built_in_document_properties.last_printed)
else:
    self.assertEqual(last_printed, doc.built_in_document_properties.last_printed)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

