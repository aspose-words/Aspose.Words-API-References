---
title: Field.is_dirty property
linktitle: is_dirty property
articleTitle: is_dirty property
second_title: Aspose.Words for Python
description: "Field.is_dirty property. Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document."
type: docs
weight: 40
url: /ru/python-net/aspose.words.fields/field/is_dirty/
---

## Field.is_dirty property

Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.


```python
@property
def is_dirty(self) -> bool:
    ...

@is_dirty.setter
def is_dirty(self, value: bool):
    ...

```

### Examples

Shows how to use special property for updating field result.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Получите значение встроенного свойства "Author" документа, а затем отобразите его с помощью поля.
doc.built_in_document_properties.author = 'John Doe'
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
self.assertFalse(field.is_dirty)
self.assertEqual('John Doe', field.result)
# Обновите свойство. Поле всё ещё отображает старое значение.
doc.built_in_document_properties.author = 'John & Jane Doe'
self.assertEqual('John Doe', field.result)
# Поскольку значение поля устарело, мы можем пометить его как "dirty".
# Это значение останется устаревшим, пока мы не обновим поле вручную с помощью метода Field.Update().
field.is_dirty = True
with io.BytesIO() as doc_stream:
    # Если мы сохраним без вызова метода обновления,
    # поле будет продолжать отображать устаревшее значение в результирующем документе.
    doc.save(stream=doc_stream, save_format=aw.SaveFormat.DOCX)
    # Объект LoadOptions имеет параметр для обновления всех полей
    # отмеченных как "dirty" при загрузке документа.
    options = aw.loading.LoadOptions()
    options.update_dirty_fields = update_dirty_fields
    doc = aw.Document(stream=doc_stream, load_options=options)
    self.assertEqual('John & Jane Doe', doc.built_in_document_properties.author)
    field = doc.range.fields[0].as_field_author()
    # Обновление таких "dirty" полей автоматически сбрасывает их флаг "IsDirty" в false.
    if update_dirty_fields:
        self.assertEqual('John & Jane Doe', field.result)
        self.assertFalse(field.is_dirty)
    else:
        self.assertEqual('John Doe', field.result)
        self.assertTrue(field.is_dirty)
```

### See Also

* module [aspose.words.fields](../../)
* class [Field](../)

