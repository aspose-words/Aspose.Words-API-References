---
title: FieldPageRef.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldPageRef.bookmark_name property. Gets or sets the name of the bookmark."
type: docs
weight: 20
url: /ar/python-net/aspose.words.fields/fieldpageref/bookmark_name/
---

## FieldPageRef.bookmark_name property

Gets or sets the name of the bookmark.


```python
@property
def bookmark_name(self) -> str:
    ...

@bookmark_name.setter
def bookmark_name(self, value: str):
    ...

```

### Examples

Shows to insert PAGEREF fields to display the relative location of bookmarks.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
ExField._insert_and_name_bookmark(builder, 'MyBookmark1')
# أدرج حقل PAGEREF يعرض الصفحة التي توجد عليها إشارة مرجعية.
# اضبط علامة InsertHyperlink لجعل الحقل يعمل أيضًا كرابط قابل للنقر إلى الإشارة المرجعية.
self.assertEqual(' PAGEREF  MyBookmark3 \\h', ExField._insert_field_page_ref(builder, 'MyBookmark3', True, False, 'Hyperlink to Bookmark3, on page: ').get_field_code())
# يمكننا استخدام العلامة \p لجعل حقل PAGEREF يعرض
# موضع الإشارة المرجعية بالنسبة إلى موضع الحقل.
# الإشارة المرجعية Bookmark1 على نفس الصفحة وفوق هذا الحقل، لذا ستكون النتيجة المعروضة لهذا الحقل "above".
self.assertEqual(' PAGEREF  MyBookmark1 \\h \\p', ExField._insert_field_page_ref(builder, 'MyBookmark1', True, True, 'Bookmark1 is ').get_field_code())
# الإشارة المرجعية Bookmark2 ستكون على نفس الصفحة وتحت هذا الحقل، لذا ستكون النتيجة المعروضة لهذا الحقل "below".
self.assertEqual(' PAGEREF  MyBookmark2 \\h \\p', ExField._insert_field_page_ref(builder, 'MyBookmark2', True, True, 'Bookmark2 is ').get_field_code())
# الإشارة المرجعية Bookmark3 ستكون على صفحة مختلفة، لذا سيعرض الحقل "on page 2".
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

