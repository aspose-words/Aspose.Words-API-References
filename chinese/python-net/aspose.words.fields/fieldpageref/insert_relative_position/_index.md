---
title: FieldPageRef.insert_relative_position property
linktitle: insert_relative_position property
articleTitle: insert_relative_position property
second_title: Aspose.Words for Python
description: "FieldPageRef.insert_relative_position property. Gets or sets whether to insert a relative position of the bookmarked paragraph."
type: docs
weight: 40
url: /zh/python-net/aspose.words.fields/fieldpageref/insert_relative_position/
---

## FieldPageRef.insert_relative_position property

Gets or sets whether to insert a relative position of the bookmarked paragraph.


```python
@property
def insert_relative_position(self) -> bool:
    ...

@insert_relative_position.setter
def insert_relative_position(self, value: bool):
    ...

```

### Examples

Shows to insert PAGEREF fields to display the relative location of bookmarks.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
ExField._insert_and_name_bookmark(builder, 'MyBookmark1')
# 插入一个 PAGEREF 字段，以显示书签所在的页码。
# 设置 InsertHyperlink 标志，使该字段还能作为指向书签的可点击链接。
self.assertEqual(' PAGEREF  MyBookmark3 \\h', ExField._insert_field_page_ref(builder, 'MyBookmark3', True, False, 'Hyperlink to Bookmark3, on page: ').get_field_code())
# 我们可以使用 \p 标志让 PAGEREF 字段显示
# 书签相对于字段位置的相对位置。
# Bookmark1 位于同一页且在此字段上方，因此该字段显示的结果将是 "above"。
self.assertEqual(' PAGEREF  MyBookmark1 \\h \\p', ExField._insert_field_page_ref(builder, 'MyBookmark1', True, True, 'Bookmark1 is ').get_field_code())
# Bookmark2 位于同一页且在此字段下方，因此该字段显示的结果将是 "below"。
self.assertEqual(' PAGEREF  MyBookmark2 \\h \\p', ExField._insert_field_page_ref(builder, 'MyBookmark2', True, True, 'Bookmark2 is ').get_field_code())
# Bookmark3 将位于不同的页码，因此字段将显示 "on page 2"。
self.assertEqual(' PAGEREF  MyBookmark3 \\h \\p', ExField._insert_field_page_ref(builder, 'MyBookmark3', True, True, 'Bookmark3 is ').get_field_code())
ExField._insert_and_name_bookmark(builder, 'MyBookmark2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
ExField._insert_and_name_bookmark(builder, 'MyBookmark3')
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.PAGEREF.docx')
```

Shows to insert PAGEREF fields to display the relative location of bookmarks (InsertFieldPageRef).

```python
@staticmethod
def _insert_field_page_ref(builder, bookmark_name, insert_hyperlink, insert_relative_position, text_before):
    builder.write(text_before)
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_PAGE_REF, update_field=True).as_field_page_ref()
    field.bookmark_name = bookmark_name
    field.insert_hyperlink = insert_hyperlink
    field.insert_relative_position = insert_relative_position
    builder.writeln()
    return field

@staticmethod
def _insert_and_name_bookmark(builder, bookmark_name):
    builder.start_bookmark(bookmark_name)
    builder.writeln(f'Contents of bookmark "{bookmark_name}".')
    builder.end_bookmark(bookmark_name)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldPageRef](../)

