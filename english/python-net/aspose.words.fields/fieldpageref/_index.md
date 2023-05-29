﻿---
title: FieldPageRef class
linktitle: FieldPageRef class
articleTitle: FieldPageRef class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldPageRef class. Implements the PAGEREF field"
type: docs
weight: 810
url: /python-net/aspose.words.fields/fieldpageref/
---

## FieldPageRef class

Implements the PAGEREF field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Inserts the number of the page containing the specified bookmark for a cross-reference.


**Inheritance:** [FieldPageRef](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldPageRef()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets the name of the bookmark. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [insert_hyperlink](./insert_hyperlink/) | Gets or sets whether to insert a hyperlink to the bookmarked paragraph. |
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

Shows to insert PAGEREF fields to display the relative location of bookmarks.

```python
def test_field_page_ref(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    ExField.insert_and_name_bookmark(builder, "MyBookmark1")

    # Insert a PAGEREF field that displays what page a bookmark is on.
    # Set the InsertHyperlink flag to make the field also function as a clickable link to the bookmark.
    self.assertEqual(" PAGEREF  MyBookmark3 \\h",
        ExField.insert_field_page_ref(builder, "MyBookmark3", True, False, "Hyperlink to Bookmark3, on page: ").get_field_code())

    # We can use the \p flag to get the PAGEREF field to display
    # the bookmark's position relative to the position of the field.
    # Bookmark1 is on the same page and above this field, so this field's displayed result will be "above".
    self.assertEqual(" PAGEREF  MyBookmark1 \\h \\p",
        ExField.insert_field_page_ref(builder, "MyBookmark1", True, True, "Bookmark1 is ").get_field_code())

    # Bookmark2 will be on the same page and below this field, so this field's displayed result will be "below".
    self.assertEqual(" PAGEREF  MyBookmark2 \\h \\p",
        ExField.insert_field_page_ref(builder, "MyBookmark2", True, True, "Bookmark2 is ").get_field_code())

    # Bookmark3 will be on a different page, so the field will display "on page 2".
    self.assertEqual(" PAGEREF  MyBookmark3 \\h \\p",
        ExField.insert_field_page_ref(builder, "MyBookmark3", True, True, "Bookmark3 is ").get_field_code())

    ExField.insert_and_name_bookmark(builder, "MyBookmark2")
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    ExField.insert_and_name_bookmark(builder, "MyBookmark3")

    doc.update_page_layout()
    doc.update_fields()
    doc.save(ARTIFACTS_DIR + "Field.field_page_ref.docx")

@staticmethod
def insert_field_page_ref(builder: aw.DocumentBuilder, bookmark_name: str, insert_hyperlink: bool, insert_relative_position: bool, text_before: str) -> aw.fields.FieldPageRef:
    """Uses a document builder to insert a PAGEREF field and sets its properties."""

    builder.write(text_before)

    field = builder.insert_field(aw.fields.FieldType.FIELD_PAGE_REF, True).as_field_page_ref()
    field.bookmark_name = bookmark_name
    field.insert_hyperlink = insert_hyperlink
    field.insert_relative_position = insert_relative_position
    builder.writeln()

    return field

@staticmethod
def insert_and_name_bookmark(builder: aw.DocumentBuilder, bookmark_name: str):
    """Uses a document builder to insert a named bookmark."""

    builder.start_bookmark(bookmark_name)
    builder.writeln(f"Contents of bookmark \"{bookmark_name}\".")
    builder.end_bookmark(bookmark_name)
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

