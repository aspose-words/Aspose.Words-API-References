---
title: FieldXE.page_range_bookmark_name property
linktitle: page_range_bookmark_name property
articleTitle: page_range_bookmark_name property
second_title: Aspose.Words for Python
description: "FieldXE.page_range_bookmark_name property. Gets or sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number."
type: docs
weight: 60
url: /ru/python-net/aspose.words.fields/fieldxe/page_range_bookmark_name/
---

## FieldXE.page_range_bookmark_name property

Gets or sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number.


```python
@property
def page_range_bookmark_name(self) -> str:
    ...

@page_range_bookmark_name.setter
def page_range_bookmark_name(self, value: str):
    ...

```

### Examples

Shows how to specify a bookmark's spanned pages as a page range for an INDEX field entry.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Создайте поле INDEX, которое отобразит запись для каждого найденного в документе поля XE.
# Каждая запись будет отображать значение свойства Text поля XE слева,
# а номер страницы, содержащей поле XE, — справа.
# Элемент INDEX соберёт все поля XE с совпадающими значениями в свойстве "Text"
# в одну запись, а не создавать отдельную запись для каждого поля XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Для записей INDEX, отображающих диапазоны страниц, мы можем указать строку-разделитель
# которая будет появляться между номером первой страницы и номером последней.
index.page_number_separator = ', on page(s) '
index.page_range_separator = ' to '
self.assertEqual(' INDEX  \\e ", on page(s) " \\g " to "', index.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'My entry'
# Если поле XE задает закладку с помощью свойства PageRangeBookmarkName,
# его запись INDEX покажет диапазон страниц, охватываемый закладкой
# вместо номера страницы, содержащей поле XE.
index_entry.page_range_bookmark_name = 'MyBookmark'
self.assertEqual(' XE  "My entry" \\r MyBookmark', index_entry.get_field_code())
self.assertEqual('MyBookmark', index_entry.page_range_bookmark_name)
# Вставьте закладку, начинающуюся на странице 3 и заканчивающуюся на странице 5.
# Запись INDEX для поля XE, ссылающегося на эту закладку, отобразит этот диапазон страниц.
# В нашей таблице запись INDEX отобразит "My entry, on page(s) 3 to 5".
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('MyBookmark')
builder.write('Start of MyBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('End of MyBookmark')
builder.end_bookmark('MyBookmark')
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.PageRangeBookmark.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldXE](../)

