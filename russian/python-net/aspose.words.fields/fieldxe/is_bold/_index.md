---
title: FieldXE.is_bold property
linktitle: is_bold property
articleTitle: is_bold property
second_title: Aspose.Words for Python
description: "FieldXE.is_bold property. Gets or sets whether to apply bold formatting to the entry's page number."
type: docs
weight: 30
url: /ru/python-net/aspose.words.fields/fieldxe/is_bold/
---

## FieldXE.is_bold property

Gets or sets whether to apply bold formatting to the entry's page number.


```python
@property
def is_bold(self) -> bool:
    ...

@is_bold.setter
def is_bold(self, value: bool):
    ...

```

### Examples

Shows how to populate an INDEX field with entries using XE fields, and also modify its appearance.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Создайте поле INDEX, которое отобразит запись для каждого найденного в документе поля XE.
# Каждая запись будет отображать значение свойства Text поля XE слева,
# а номер страницы, содержащей поле XE, — справа.
# Если у полей XE одинаковое значение в их свойстве "Text",
# поле INDEX сгруппирует их в одну запись.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.language_id = '1033'
# Установка значения этого свойства в "A" сгруппирует все записи по первой букве,
# и разместит эту букву в верхнем регистре над каждой группой.
index.heading = 'A'
# Установите, чтобы таблица, созданная полем INDEX, охватывала 2 столбца.
index.number_of_columns = '2'
# Установите, чтобы любые записи, начинающиеся с букв вне диапазона "a-c", были опущены.
index.letter_range = 'a-c'
self.assertEqual(' INDEX  \\z 1033 \\h A \\c 2 \\p a-c', index.get_field_code())
# Следующие два поля XE появятся под заголовком "A",
# при этом их соответствующее форматирование текста также будет применено к номерам страниц.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apple'
index_entry.is_italic = True
self.assertEqual(' XE  Apple \\i', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apricot'
index_entry.is_bold = True
self.assertEqual(' XE  Apricot \\b', index_entry.get_field_code())
# Оба следующих поля XE будут под заголовками "B" и "C" в оглавлении таблицы полей INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Banana'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cherry'
# Поля INDEX сортируют все записи в алфавитном порядке, поэтому эта запись появится под "A" вместе с другими двумя.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Avocado'
# Эта запись не появится, потому что она начинается с буквы "D",
# что находится за пределами диапазона символов "a-c", определяемого свойством LetterRange поля INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Durian'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Formatting.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldXE](../)

