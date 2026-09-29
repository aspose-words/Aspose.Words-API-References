---
title: FieldIndex.has_sequence_name property
linktitle: has_sequence_name property
articleTitle: has_sequence_name property
second_title: Aspose.Words for Python
description: "FieldIndex.has_sequence_name property. Gets a value indicating whether a sequence should be used while the field's result building."
type: docs
weight: 60
url: /ru/python-net/aspose.words.fields/fieldindex/has_sequence_name/
---

## FieldIndex.has_sequence_name property

Gets a value indicating whether a sequence should be used while the field's result building.


```python
@property
def has_sequence_name(self) -> bool:
    ...

```

### Examples

Shows how to split a document into portions by combining INDEX and SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Создайте поле INDEX, которое отобразит запись для каждого найденного в документе поля XE.
# Каждая запись будет отображать значение свойства Text поля XE слева,
# а номер страницы, содержащей поле XE, — справа.
# Если у полей XE одинаковое значение в их свойстве "Text",
# поле INDEX сгруппирует их в одну запись.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# В свойстве SequenceName задайте имя последовательности SEQ‑полей. Каждая запись этого поля INDEX теперь также будет отображать
# номер, на котором находится счётчик последовательности в месте XE‑поля, создавшего эту запись.
index.sequence_name = 'MySequence'
# Установите текст, который будет окружать последовательность и номера страниц, чтобы объяснить их значение пользователю.
# Запись, созданная с этой конфигурацией, будет отображать что‑то вроде "MySequence at 1 on page 1" рядом с номером страницы.
# PageNumberSeparator и SequenceSeparator не могут быть длиннее 15 символов.
index.page_number_separator = '\tMySequence at '
index.sequence_separator = ' on page '
self.assertTrue(index.has_sequence_name)
self.assertEqual(' INDEX  \\s MySequence \\e "\tMySequence at " \\d " on page "', index.get_field_code())
# Поля SEQ отображают счётчик, который увеличивается у каждого поля SEQ.
# Эти поля также поддерживают отдельные счётчики для каждой уникальной именованной последовательности
# идентифицируемой свойством "SequenceIdentifier" поля SEQ.
# Вставьте SEQ‑поле, которое перемещает последовательность "MySequence" к 1.
# Это поле не отличается от обычного текста документа. Оно не будет отображаться в оглавлении поля INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', sequence_field.get_field_code())
# Вставьте XE‑поле, которое создаст запись в поле INDEX.
# Поскольку "MySequence" находится на 1, а это XE‑поле — на странице 2, вместе с пользовательскими разделителями, определёнными выше,
# запись INDEX этого поля отобразит "Cat" слева и "MySequence at 1 on page 2" справа.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
self.assertEqual(' XE  Cat', index_entry.get_field_code())
# Вставьте разрыв страницы и используйте SEQ‑поля, чтобы продвинуть "MySequence" до 3.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
# Вставьте XE‑поле с тем же свойством Text, что и выше.
# Запись INDEX будет группировать поля XE с совпадающими значениями в свойстве "Text"
# в одну запись, а не создавать отдельную запись для каждого поля XE.
# Поскольку мы на странице 2 и "MySequence" равно 3, ", 3 on page 3" будет добавлено к той же записи INDEX, что выше.
# Часть с номером страницы этой записи INDEX теперь будет отображать "MySequence at 1 on page 2, 3 on page 3".
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
# Вставьте XE‑поле с новым и уникальным значением свойства Text.
# Это добавит новую запись, где MySequence находится на 3 на странице 4.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Dog'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Sequence.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

