---
title: FieldIndex.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldIndex.bookmark_name property. Gets or sets the name of the bookmark that marks the portion of the document used to build the index."
type: docs
weight: 20
url: /ru/python-net/aspose.words.fields/fieldindex/bookmark_name/
---

## FieldIndex.bookmark_name property

Gets or sets the name of the bookmark that marks the portion of the document used to build the index.


```python
@property
def bookmark_name(self) -> str:
    ...

@bookmark_name.setter
def bookmark_name(self, value: str):
    ...

```

### Examples

Shows how to create an INDEX field, and then use XE fields to populate it with entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Создайте поле INDEX, которое отобразит запись для каждого найденного в документе поля XE.
# Каждая запись будет показывать значение свойства Text поля XE слева
# и страницу, содержащую поле XE, справа.
# Если у полей XE одинаковое значение в их свойстве "Text",
# поле INDEX сгруппирует их в одну запись.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Настройте поле INDEX так, чтобы оно отображало только поля XE, находящиеся в пределах
# закладки с именем "MainBookmark" и у которых свойства "EntryType" имеют значение "A".
# Для полей INDEX и XE свойство "EntryType" использует только первый символ строкового значения.
index.bookmark_name = 'MainBookmark'
index.entry_type = 'A'
self.assertEqual(' INDEX  \\b MainBookmark \\f A', index.get_field_code())
# На новой странице начните закладку с именем, которое соответствует значению
# свойства "BookmarkName" поля INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('MainBookmark')
# Поле INDEX подхватит эту запись, потому что она находится внутри закладки,
# и её тип записи также совпадает с типом записи поля INDEX.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 1'
index_entry.entry_type = 'A'
self.assertEqual(' XE  "Index entry 1" \\f A', index_entry.get_field_code())
# Вставьте поле XE, которое не появится в INDEX, потому что типы записей не совпадают.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 2'
index_entry.entry_type = 'B'
# Закончите закладку и вставьте поле XE после неё.
# Оно того же типа, что и поле INDEX, но не будет отображаться
# поскольку он находится за пределами границ закладки.
builder.end_bookmark('MainBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 3'
index_entry.entry_type = 'A'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Filtering.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

