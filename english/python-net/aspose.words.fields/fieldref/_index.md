---
title: FieldRef class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the REF field."
type: docs
weight: 870
url: /python-net/aspose.words.fields/fieldref/
---

## FieldRef class

Implements the REF field.


Inserts the text or graphics represented by the specified bookmark.


**Inheritance:** [FieldRef](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldRef()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets the referenced bookmark's name. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [include_note_or_comment](./include_note_or_comment/) | Gets or sets whether to increment footnote, endnote, and annotation numbers that are marked by the bookmark, and insert the corresponding footnote, endnote, and comment text. |
| [insert_hyperlink](./insert_hyperlink/) | Gets or sets whether to create a hyperlink to the bookmarked paragraph. |
| [insert_paragraph_number](./insert_paragraph_number/) | Gets or sets whether to insert the paragraph number of the referenced paragraph exactly as it appears in the document. |
| [insert_paragraph_number_in_full_context](./insert_paragraph_number_in_full_context/) | Gets or sets whether to insert the paragraph number of the referenced paragraph in full context. |
| [insert_paragraph_number_in_relative_context](./insert_paragraph_number_in_relative_context/) | Gets or sets whether to insert the paragraph number of the referenced paragraph in relative context. |
| [insert_relative_position](./insert_relative_position/) | Gets or sets whether to insert the relative position of the referenced paragraph. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [number_separator](./number_separator/) | Gets or sets the character sequence that is used to separate sequence numbers and page numbers. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be null.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [suppress_non_delimiters](./suppress_non_delimiters/) | Gets or sets whether to suppress non-delimiter characters. |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### Examples

Shows how to insert REF fields to reference bookmarks.

```python
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

* module [aspose.words.fields](../)
* class [Field](../field/)

