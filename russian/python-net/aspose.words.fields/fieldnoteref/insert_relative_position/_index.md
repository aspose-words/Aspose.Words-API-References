---
title: FieldNoteRef.insert_relative_position property
linktitle: insert_relative_position property
articleTitle: insert_relative_position property
second_title: Aspose.Words for Python
description: "FieldNoteRef.insert_relative_position property. Gets or sets whether to insert a relative position of the bookmarked paragraph."
type: docs
weight: 50
url: /ru/python-net/aspose.words.fields/fieldnoteref/insert_relative_position/
---

## FieldNoteRef.insert_relative_position property

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

Shows to insert NOTEREF fields, and modify their appearance.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Создайте закладку с сноской, на которую будет ссылаться поле NOTEREF.
ExField._insert_bookmark_with_footnote(builder, 'MyBookmark1', 'Contents of MyBookmark1', 'Footnote from MyBookmark1')
# Это поле NOTEREF отобразит номер сноски внутри указанной закладки.
# Установка свойства InsertHyperlink позволяет перейти к закладке, используя Ctrl + щелчок по полю в Microsoft Word.
self.assertEqual(' NOTEREF  MyBookmark2 \\h', ExField._insert_field_note_ref(builder, 'MyBookmark2', True, False, False, 'Hyperlink to Bookmark2, with footnote number ').get_field_code())
# При использовании флага \p после номера сноски поле также отображает позицию закладки относительно поля.
# Bookmark1 находится над этим полем и содержит номер сноски 1, поэтому при обновлении результат будет "1 выше".
self.assertEqual(' NOTEREF  MyBookmark1 \\h \\p', ExField._insert_field_note_ref(builder, 'MyBookmark1', True, True, False, 'Bookmark1, with footnote number ').get_field_code())
# Bookmark2 находится под этим полем и содержит номер сноски 2, поэтому поле отобразит "2 ниже".
# Флаг \f заставляет номер 2 отображаться в том же формате, что и метка номера сноски в реальном тексте.
self.assertEqual(' NOTEREF  MyBookmark2 \\h \\p \\f', ExField._insert_field_note_ref(builder, 'MyBookmark2', True, True, True, 'Bookmark2, with footnote number ').get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
ExField._insert_bookmark_with_footnote(builder, 'MyBookmark2', 'Contents of MyBookmark2', 'Footnote from MyBookmark2')
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.NOTEREF.docx')
```

Shows to insert NOTEREF fields, and modify their appearance (InsertFieldNoteRef).

```python
@staticmethod
def _insert_field_note_ref(builder, bookmark_name, insert_hyperlink, insert_relative_position, insert_reference_mark, text_before):
    builder.write(text_before)
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_NOTE_REF, update_field=True).as_field_note_ref()
    field.bookmark_name = bookmark_name
    field.insert_hyperlink = insert_hyperlink
    field.insert_relative_position = insert_relative_position
    field.insert_reference_mark = insert_reference_mark
    builder.writeln()
    return field

@staticmethod
def _insert_bookmark_with_footnote(builder, bookmark_name, bookmark_text, footnote_text):
    builder.start_bookmark(bookmark_name)
    builder.write(bookmark_text)
    builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text=footnote_text)
    builder.end_bookmark(bookmark_name)
    builder.writeln()
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldNoteRef](../)

