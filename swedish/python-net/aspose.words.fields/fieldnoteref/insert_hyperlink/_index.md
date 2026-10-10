---
title: FieldNoteRef.insert_hyperlink property
linktitle: insert_hyperlink property
articleTitle: insert_hyperlink property
second_title: Aspose.Words for Python
description: "FieldNoteRef.insert_hyperlink property. Gets or sets whether to insert a hyperlink to the bookmarked paragraph."
type: docs
weight: 30
url: /sv/python-net/aspose.words.fields/fieldnoteref/insert_hyperlink/
---

## FieldNoteRef.insert_hyperlink property

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

Shows to insert NOTEREF fields, and modify their appearance.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Skapa ett bokmärke med en fotnot som NOTEREF-fältet kommer att referera till.
ExField._insert_bookmark_with_footnote(builder, 'MyBookmark1', 'Contents of MyBookmark1', 'Footnote from MyBookmark1')
# Detta NOTEREF-fält kommer att visa numret på fotnoten i det refererade bokmärket.
# Genom att ställa in egenskapen InsertHyperlink kan vi hoppa till bokmärket genom att Ctrl‑klicka på fältet i Microsoft Word.
self.assertEqual(' NOTEREF  MyBookmark2 \\h', ExField._insert_field_note_ref(builder, 'MyBookmark2', True, False, False, 'Hyperlink to Bookmark2, with footnote number ').get_field_code())
# När \p-flaggan används visar fältet efter fotnotens nummer även bokmärkets position relativt fältet.
# Bookmark1 ligger ovanför detta fält och innehåller fotnotnummer 1, så resultatet blir "1 above" vid uppdatering.
self.assertEqual(' NOTEREF  MyBookmark1 \\h \\p', ExField._insert_field_note_ref(builder, 'MyBookmark1', True, True, False, 'Bookmark1, with footnote number ').get_field_code())
# Bookmark2 ligger under detta fält och innehåller fotnotnummer 2, så fältet visar "2 below".
# Flaggan \f får talet 2 att visas i samma format som fotnotens nummeretikett i den faktiska texten.
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

