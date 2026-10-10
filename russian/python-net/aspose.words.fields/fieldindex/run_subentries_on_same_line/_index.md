---
title: FieldIndex.run_subentries_on_same_line property
linktitle: run_subentries_on_same_line property
articleTitle: run_subentries_on_same_line property
second_title: Aspose.Words for Python
description: "FieldIndex.run_subentries_on_same_line property. Gets or sets whether run subentries into the same line as the main entry."
type: docs
weight: 140
url: /ru/python-net/aspose.words.fields/fieldindex/run_subentries_on_same_line/
---

## FieldIndex.run_subentries_on_same_line property

Gets or sets whether run subentries into the same line as the main entry.


```python
@property
def run_subentries_on_same_line(self) -> bool:
    ...

@run_subentries_on_same_line.setter
def run_subentries_on_same_line(self, value: bool):
    ...

```

### Examples

Shows how to work with subentries in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Создайте поле INDEX, которое отобразит запись для каждого найденного в документе поля XE.
# Каждая запись будет отображать значение свойства Text поля XE слева,
# а номер страницы, содержащей поле XE, — справа.
# Элемент INDEX соберёт все поля XE с совпадающими значениями в свойстве "Text"
# в одну запись, а не создавать отдельную запись для каждого поля XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.page_number_separator = ', see page '
index.heading = 'A'
# XE‑поля, у которых свойство Text имеет значение, становящееся заголовком записи INDEX.
# Если это значение содержит два строковых сегмента, разделённых двоеточием (INDEX‑запись будет рассматривать :) как разделитель,
# первый сегмент — заголовок, а второй сегмент станет подзаголовком.
# Поле INDEX сначала группирует записи в алфавитном порядке, затем, если есть несколько XE‑полей с одинаковыми
# заголовками, поле INDEX дополнительно подразделит их по значениям этих заголовков.
# Может быть несколько уровней подразделения, в зависимости от того, сколько раз
# свойства Text XE‑полей разбиваются таким образом.
# По умолчанию, группа записей поля INDEX создаёт новую строку для каждого подзаголовка в этой группе.
# Мы можем установить флаг RunSubentriesOnSameLine в значение true, чтобы сохранить заголовок,
# и каждый подзаголовок группы в одной строке, что сделает поле INDEX более компактным.
index.run_subentries_on_same_line = run_subentries_on_the_same_line
if run_subentries_on_the_same_line:
    self.assertEqual(' INDEX  \\e ", see page " \\h A \\r', index.get_field_code())
else:
    self.assertEqual(' INDEX  \\e ", see page " \\h A', index.get_field_code())
# Вставьте два поля XE, каждое на новой странице, с одинаковым заголовком под названием "Heading 1",
# которые поле INDEX использует для их группировки.
# Если RunSubentriesOnSameLine равно false, то таблица INDEX создаст три строки:
# одна строка для группирующего заголовка "Heading 1", и ещё одна строка для каждого подзаголовка.
# Если RunSubentriesOnSameLine равно true, то таблица INDEX создаст одну строку
# записи, охватывающую заголовок и каждый подзаголовок.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Heading 1:Subheading 1'
self.assertEqual(' XE  "Heading 1:Subheading 1"', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Heading 1:Subheading 2'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + f'Field.INDEX.XE.Subheading.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

