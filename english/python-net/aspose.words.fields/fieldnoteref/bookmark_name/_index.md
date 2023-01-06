---
title: bookmark_name property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the name of the bookmark."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldnoteref/bookmark_name/
---

## FieldNoteRef.bookmark_name property

Gets or sets the name of the bookmark.


### Examples

Shows to insert NOTEREF fields, and modify their appearance.

```python
def test_field_note_ref(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    # Create a bookmark with a footnote that the NOTEREF field will reference.
    ExField.insert_bookmark_with_footnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1")

    # This NOTEREF field will display the number of the footnote inside the referenced bookmark.
    # Setting the "insert_hyperlink" property lets us jump to the bookmark by Ctrl + clicking the field in Microsoft Word.
    self.assertEqual(" NOTEREF  MyBookmark2 \\h",
        ExField.insert_field_note_ref(builder, "MyBookmark2", True, False, False, "Hyperlink to Bookmark2, with footnote number ").get_field_code())

    # When using the \p flag, after the footnote number, the field also displays the bookmark's position relative to the field.
    # Bookmark1 is above this field and contains footnote number 1, so the result will be "1 above" on update.
    self.assertEqual(" NOTEREF  MyBookmark1 \\h \\p",
        ExField.insert_field_note_ref(builder, "MyBookmark1", True, True, False, "Bookmark1, with footnote number ").get_field_code())

    # Bookmark2 is below this field and contains footnote number 2, so the field will display "2 below".
    # The \f flag makes the number 2 appear in the same format as the footnote number label in the actual text.
    self.assertEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        ExField.insert_field_note_ref(builder, "MyBookmark2", True, True, True, "Bookmark2, with footnote number ").get_field_code())

    builder.insert_break(aw.BreakType.PAGE_BREAK)
    ExField.insert_bookmark_with_footnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2")

    doc.update_page_layout()
    doc.update_fields()
    doc.save(ARTIFACTS_DIR + "Field.field_note_ref.docx")

@staticmethod
def insert_field_note_ref(builder: aw.DocumentBuilder, bookmark_name: str, insert_hyperlink: bool, insert_relative_position: bool, insert_reference_mark: bool, text_before: str) -> aw.fields.FieldNoteRef:
    """Uses a document builder to insert a NOTEREF field with specified properties."""

    builder.write(text_before)

    field = builder.insert_field(aw.fields.FieldType.FIELD_NOTE_REF, True).as_field_note_ref()
    field.bookmark_name = bookmark_name
    field.insert_hyperlink = insert_hyperlink
    field.insert_relative_position = insert_relative_position
    field.insert_reference_mark = insert_reference_mark
    builder.writeln()

    return field

@staticmethod
def insert_bookmark_with_footnote(builder: aw.DocumentBuilder, bookmark_name: str, bookmark_text: str, footnote_text: str):
    """Uses a document builder to insert a named bookmark with a footnote at the end."""

    builder.start_bookmark(bookmark_name)
    builder.write(bookmark_text)
    builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, footnote_text)
    builder.end_bookmark(bookmark_name)
    builder.writeln()
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldNoteRef](../)

