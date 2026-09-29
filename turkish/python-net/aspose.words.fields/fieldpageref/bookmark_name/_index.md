---
title: FieldPageRef.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldPageRef.bookmark_name property. Gets or sets the name of the bookmark."
type: docs
weight: 20
url: /tr/python-net/aspose.words.fields/fieldpageref/bookmark_name/
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
# Bir yer işaretinin hangi sayfada olduğunu gösteren bir PAGEREF alanı ekleyin.
# Alanı aynı zamanda yer işaretine tıklanabilir bir bağlantı olarak işlev görmesi için InsertHyperlink bayrağını ayarlayın.
self.assertEqual(' PAGEREF  MyBookmark3 \\h', ExField._insert_field_page_ref(builder, 'MyBookmark3', True, False, 'Hyperlink to Bookmark3, on page: ').get_field_code())
# PAGEREF alanının görüntülemesini sağlamak için \p bayrağını kullanabiliriz
# alanın konumuna göre yer işaretinin konumunu.
# Bookmark1 aynı sayfada ve bu alanın üstünde, bu yüzden bu alanın gösterilen sonucu "above" olacaktır.
self.assertEqual(' PAGEREF  MyBookmark1 \\h \\p', ExField._insert_field_page_ref(builder, 'MyBookmark1', True, True, 'Bookmark1 is ').get_field_code())
# Bookmark2 aynı sayfada ve bu alanın altında olacak, bu yüzden bu alanın gösterilen sonucu "below" olacaktır.
self.assertEqual(' PAGEREF  MyBookmark2 \\h \\p', ExField._insert_field_page_ref(builder, 'MyBookmark2', True, True, 'Bookmark2 is ').get_field_code())
# Bookmark3 farklı bir sayfada olacak, bu yüzden alan "on page 2" gösterecek.
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

