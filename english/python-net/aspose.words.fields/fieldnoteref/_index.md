﻿---
title: FieldNoteRef class
linktitle: FieldNoteRef class
articleTitle: FieldNoteRef class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldNoteRef class. Implements the NOTEREF field"
type: docs
weight: 740
url: /python-net/aspose.words.fields/fieldnoteref/
---

## FieldNoteRef class

Implements the NOTEREF field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Inserts the mark of the footnote or endnote that is marked by the specified bookmark.


**Inheritance:** [FieldNoteRef](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldNoteRef()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets the name of the bookmark. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [insert_hyperlink](./insert_hyperlink/) | Gets or sets whether to insert a hyperlink to the bookmarked paragraph. |
| [insert_reference_mark](./insert_reference_mark/) | Inserts the reference mark with the same character formatting as the Footnote Reference or Endnote Reference style. |
| [insert_relative_position](./insert_relative_position/) | Gets or sets whether to insert a relative position of the bookmarked paragraph. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

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

Shows how to cross-reference footnotes with the NOTEREF field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("CrossReference: ")

# <--- don't update field
field = builder.insert_field(awf.FieldType.FIELD_NOTE_REF, False)
field.bookmark_name = "CrossRefBookmark"
field.insert_hyperlink = True
field.insert_reference_mark = True
field.insert_relative_position = False
builder.writeln()

builder.start_bookmark("CrossRefBookmark")
builder.write("Hello world!")
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "Cross referenced footnote.")
builder.end_bookmark("CrossRefBookmark")
builder.writeln()

doc.update_fields()

# This field works only in older versions of Microsoft Word.
doc.save(ARTIFACTS_DIR + "Field.field_note_ref.doc")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

