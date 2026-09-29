---
title: FieldIndex.cross_reference_separator property
linktitle: cross_reference_separator property
articleTitle: cross_reference_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.cross_reference_separator property. Gets or sets the character sequence that is used to separate cross references and other entries."
type: docs
weight: 30
url: /ru/python-net/aspose.words.fields/fieldindex/cross_reference_separator/
---

## FieldIndex.cross_reference_separator property

Gets or sets the character sequence that is used to separate cross references and other entries.


```python
@property
def cross_reference_separator(self) -> str:
    ...

@cross_reference_separator.setter
def cross_reference_separator(self, value: str):
    ...

```

### Examples

Shows how to define cross references in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Создайте поле INDEX, которое отобразит запись для каждого найденного в документе поля XE.
# Каждая запись будет отображать значение свойства Text поля XE слева,
# а номер страницы, содержащей поле XE, — справа.
# Элемент INDEX соберёт все поля XE с совпадающими значениями в свойстве "Text"
# в одну запись, а не создавать отдельную запись для каждого поля XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Мы можем настроить поле XE так, чтобы его запись INDEX отображала строку вместо номера страницы.
# Во-первых, для записей, заменяющих номер страницы строкой,
# укажите пользовательский разделитель между значением свойства Text поля XE и строкой.
index.cross_reference_separator = ', see: '
self.assertEqual(' INDEX  \\k ", see: "', index.get_field_code())
# Вставьте поле XE, которое создаёт обычную запись INDEX, отображающую номер страницы этого поля,
# и не использует значение CrossReferenceSeparator.
# Запись для этого поля XE будет отображать "Apple, 2".
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apple'
self.assertEqual(' XE  Apple', index_entry.get_field_code())
# Вставьте ещё одно поле XE на странице 3 и задайте значение свойства PageNumberReplacement.
# Это значение будет отображаться вместо номера страницы, на которой находится поле,
# и значение CrossReferenceSeparator поля INDEX появится перед ним.
# Запись для этого поля XE будет отображать "Banana, see: Tropical fruit".
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Banana'
index_entry.page_number_replacement = 'Tropical fruit'
self.assertEqual(' XE  Banana \\t "Tropical fruit"', index_entry.get_field_code())
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.CrossReferenceSeparator.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

