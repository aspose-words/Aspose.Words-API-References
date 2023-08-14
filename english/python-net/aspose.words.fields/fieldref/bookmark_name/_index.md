---
title: FieldRef.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldRef.bookmark_name property. Gets or sets the referenced bookmark's name."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldref/bookmark_name/
---

## FieldRef.bookmark_name property

Gets or sets the referenced bookmark's name.


### Examples

Shows how to insert REF fields to reference bookmarks.

```python
@unittest.skip("WORDSNET-18067")  # ExSkip
def test_field_ref(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    builder.start_bookmark("MyBookmark")
    builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "MyBookmark footnote #1")
    builder.write("Text that will appear in REF field")
    builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "MyBookmark footnote #2")
    builder.end_bookmark("MyBookmark")
    builder.move_to_document_start()

    # We will apply a custom list format, where the amount of angle brackets indicates the list level we are currently at.
    builder.list_format.apply_number_default()
    builder.list_format.list_level.number_format = "> \x0000"

    # Insert a REF field that will contain the text within our bookmark, act as a hyperlink, and clone the bookmark's footnotes.
    field = ExField.insert_field_ref(builder, "MyBookmark", "", "\n")
    field.include_note_or_comment = True
    field.insert_hyperlink = True

    self.assertEqual(" REF  MyBookmark \\f \\h", field.get_field_code())

    # Insert a REF field, and display whether the referenced bookmark is above or below it.
    field = ExField.insert_field_ref(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n")
    field.insert_relative_position = True

    self.assertEqual(" REF  MyBookmark \\p", field.get_field_code())

    # Display the list number of the bookmark as it appears in the document.
    field = ExField.insert_field_ref(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n")
    field.insert_paragraph_number = True

    self.assertEqual(" REF  MyBookmark \\n", field.get_field_code())

    # Display the bookmark's list number, but with non-delimiter characters, such as the angle brackets, omitted.
    field = ExField.insert_field_ref(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n")
    field.insert_paragraph_number = True
    field.suppress_non_delimiters = True

    self.assertEqual(" REF  MyBookmark \\n \\t", field.get_field_code())

    # Move down one list level.
    builder.list_format.list_level_number += 1
    builder.list_format.list_level.number_format = ">> \x0001"

    # Display the list number of the bookmark and the numbers of all the list levels above it.
    field = ExField.insert_field_ref(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n")
    field.insert_paragraph_number_in_full_context = True

    self.assertEqual(" REF  MyBookmark \\w", field.get_field_code())

    builder.insert_break(aw.BreakType.PAGE_BREAK)

    # Display the list level numbers between this REF field, and the bookmark that it is referencing.
    field = ExField.insert_field_ref(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n")
    field.insert_paragraph_number_in_relative_context = True

    self.assertEqual(" REF  MyBookmark \\r", field.get_field_code())

    # At the end of the document, the bookmark will show up as a list item here.
    builder.writeln("List level above bookmark")
    builder.list_format.list_level_number += 1
    builder.list_format.list_level.number_format = ">>> \x0002"

    doc.update_fields()
    doc.save(ARTIFACTS_DIR + "Field.field_ref.docx")

@staticmethod
def insert_field_ref(builder: aw.DocumentBuilder, bookmark_name: str, text_before: str, text_after: str) -> aw.fields.FieldRef:
    """Get the document builder to insert a REF field, reference a bookmark with it, and add text before and after it."""

    builder.write(text_before)
    field = builder.insert_field(aw.fields.FieldType.FIELD_REF, True).as_field_ref()
    field.bookmark_name = bookmark_name
    builder.write(text_after)
    return field
```

Shows how to create bookmarked text with a SET field, and then display it in the document using a REF field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Name bookmarked text with a SET field.
# This field refers to the "bookmark" not a bookmark structure that appears within the text, but a named variable.
field_set = builder.insert_field(aw.fields.FieldType.FIELD_SET, False).as_field_set()
field_set.bookmark_name = "MyBookmark"
field_set.bookmark_text = "Hello world!"
field_set.update()

self.assertEqual(" SET  MyBookmark \"Hello world!\"", field_set.get_field_code())

# Refer to the bookmark by name in a REF field and display its contents.
field_ref = builder.insert_field(aw.fields.FieldType.FIELD_REF, True).as_field_ref()
field_ref.bookmark_name = "MyBookmark"
field_ref.update()

self.assertEqual(" REF  MyBookmark", field_ref.get_field_code())
self.assertEqual("Hello world!", field_ref.result)

doc.save(ARTIFACTS_DIR + "Field.field_set_ref.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldRef](../)

