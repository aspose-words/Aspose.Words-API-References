---
title: FieldXE.yomi property
linktitle: yomi property
articleTitle: yomi property
second_title: Aspose.Words for Python
description: "FieldXE.yomi property. Gets or sets the yomi (first phonetic character for sorting indexes) for the index entry"
type: docs
weight: 80
url: /ru/python-net/aspose.words.fields/fieldxe/yomi/
---

## FieldXE.yomi property

Gets or sets the yomi (first phonetic character for sorting indexes) for the index entry


```python
@property
def yomi(self) -> str:
    ...

@yomi.setter
def yomi(self, value: str):
    ...

```

### Examples

Shows how to sort INDEX field entries phonetically.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Создайте поле INDEX, которое отобразит запись для каждого найденного в документе поля XE.
# Каждая запись будет отображать значение свойства Text поля XE слева,
# а номер страницы, содержащей поле XE, — справа.
# Элемент INDEX соберёт все поля XE с совпадающими значениями в свойстве "Text"
# в одну запись, а не создавать отдельную запись для каждого поля XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Таблица INDEX автоматически сортирует свои записи по значениям их свойств Text в алфавитном порядке.
# Установите таблицу INDEX так, чтобы сортировать записи фонетически, используя Хирагану.
index.use_yomi = sort_entries_using_yomi
if sort_entries_using_yomi:
    self.assertEqual(' INDEX  \\y', index.get_field_code())
else:
    self.assertEqual(' INDEX ', index.get_field_code())
# Вставьте 4 поля XE, которые будут отображаться как записи в оглавлении поля INDEX.
# Свойство "Text" может содержать написание слова кандзи, произношение которого может быть неоднозначным,
# в то время как версия слова "Yomi" будет точно отражать его произношение с использованием хираганы.
# Если мы настроим наше поле INDEX на использование Yomi, оно будет сортировать эти записи
# по значению их свойств Yomi, вместо их значений Text.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '愛子'
index_entry.yomi = 'あ'
self.assertEqual(' XE  愛子 \\y あ', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '明美'
index_entry.yomi = 'あ'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '恵美'
index_entry.yomi = 'え'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '愛美'
index_entry.yomi = 'え'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Yomi.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldXE](../)

