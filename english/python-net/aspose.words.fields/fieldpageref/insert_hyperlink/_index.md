---
title: FieldPageRef.insert_hyperlink property
linktitle: insert_hyperlink property
articleTitle: insert_hyperlink property
second_title: Aspose.Words for Python
description: "FieldPageRef.insert_hyperlink property. Gets or sets whether to insert a hyperlink to the bookmarked paragraph."
type: docs
weight: 30
url: /python-net/aspose.words.fields/fieldpageref/insert_hyperlink/
---

## FieldPageRef.insert_hyperlink property

Gets or sets whether to insert a hyperlink to the bookmarked paragraph.


```python
@property
def insert_hyperlink(self) -> bool:
    ...

@insert_hyperlink.setter
def insert_hyperlink(self, value: bool):
    ...

```

### Examples

Shows to insert PAGEREF fields to display the relative location of bookmarks.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
ExField._insert_and_name_bookmark(builder, 'MyBookmark1')
# Insert a PAGEREF field that displays what page a bookmark is on.
# Set the InsertHyperlink flag to make the field also function as a clickable link to the bookmark.
self.assertEqual(' PAGEREF  MyBookmark3 \\h', ExField._insert_field_page_ref(builder, 'MyBookmark3', True, False, 'Hyperlink to Bookmark3, on page: ').get_field_code())
# We can use the \p flag to get the PAGEREF field to display
# the bookmark's position relative to the position of the field.
# Bookmark1 is on the same page and above this field, so this field's displayed result will be "above".
self.assertEqual(' PAGEREF  MyBookmark1 \\h \\p', ExField._insert_field_page_ref(builder, 'MyBookmark1', True, True, 'Bookmark1 is ').get_field_code())
# Bookmark2 will be on the same page and below this field, so this field's displayed result will be "below".
self.assertEqual(' PAGEREF  MyBookmark2 \\h \\p', ExField._insert_field_page_ref(builder, 'MyBookmark2', True, True, 'Bookmark2 is ').get_field_code())
# Bookmark3 will be on a different page, so the field will display "on page 2".
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

