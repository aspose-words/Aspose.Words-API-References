---
title: FieldNoteRef.insert_relative_position property
linktitle: insert_relative_position property
articleTitle: insert_relative_position property
second_title: Aspose.Words for Python
description: "FieldNoteRef.insert_relative_position property. Gets or sets whether to insert a relative position of the bookmarked paragraph."
type: docs
weight: 50
url: /de/python-net/aspose.words.fields/fieldnoteref/insert_relative_position/
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
# Erstellen Sie ein Lesezeichen mit einer Fußnote, auf die das NOTEREF‑Feld verweist.
ExField._insert_bookmark_with_footnote(builder, 'MyBookmark1', 'Contents of MyBookmark1', 'Footnote from MyBookmark1')
# Dieses NOTEREF‑Feld zeigt die Nummer der Fußnote im referenzierten Lesezeichen an.
# Durch das Setzen der InsertHyperlink‑Eigenschaft können wir per Strg‑Klick auf das Feld in Microsoft Word zum Lesezeichen springen.
self.assertEqual(' NOTEREF  MyBookmark2 \\h', ExField._insert_field_note_ref(builder, 'MyBookmark2', True, False, False, 'Hyperlink to Bookmark2, with footnote number ').get_field_code())
# Bei Verwendung des \p‑Schalters zeigt das Feld nach der Fußnotennummer auch die Position des Lesezeichens relativ zum Feld an.
# Bookmark1 befindet sich über diesem Feld und enthält die Fußnotennummer 1, sodass das Ergebnis nach dem Aktualisieren "1 oben" lautet.
self.assertEqual(' NOTEREF  MyBookmark1 \\h \\p', ExField._insert_field_note_ref(builder, 'MyBookmark1', True, True, False, 'Bookmark1, with footnote number ').get_field_code())
# Bookmark2 befindet sich unter diesem Feld und enthält die Fußnotennummer 2, sodass das Feld "2 unten" anzeigt.
# Der \f‑Schalter lässt die Nummer 2 im selben Format wie das Fußnotennummern‑Label im eigentlichen Text erscheinen.
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

