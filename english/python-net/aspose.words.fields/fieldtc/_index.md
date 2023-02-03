---
title: FieldTC class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the TC field"
type: docs
weight: 1020
url: /python-net/aspose.words.fields/fieldtc/
---

## FieldTC class

Implements the TC field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Defines the text and page number for a table of contents (including a table of figures) entry, which
is used by a TOC field.


**Inheritance:** [FieldTC](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldTC()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [entry_level](./entry_level/) | Gets or sets the level of the entry. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [omit_page_number](./omit_page_number/) | Gets or sets whether page number in TOC should be omitted for this field. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [text](./text/) | Gets or sets the text of the entry. |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |
| [type_identifier](./type_identifier/) | Gets or sets a type identifier for this field (which is typically a letter). |

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

Shows how to insert a TOC field, and filter which TC fields end up as entries.

```python
def test_field_toc_entry_identifier(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    # Insert a TOC field, which will compile all TC fields into a table of contents.
    field_toc = builder.insert_field(aw.fields.FieldType.FIELD_TOC, True).as_field_toc()

    # Configure the field only to pick up TC entries of the "A" type, and an entry-level between 1 and 3.
    field_toc.entry_identifier = "A"
    field_toc.entry_level_range = "1-3"

    self.assertEqual(" TOC  \\f A \\l 1-3", field_toc.get_field_code())

    # These two entries will appear in the table.
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    ExField.insert_toc_entry(builder, "TC field 1", "A", "1")
    ExField.insert_toc_entry(builder, "TC field 2", "A", "2")

    self.assertEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.range.fields[1].get_field_code())

    # This entry will be omitted from the table because it has a different type from "A".
    ExField.insert_toc_entry(builder, "TC field 3", "B", "1")

    # This entry will be omitted from the table because it has an entry-level outside of the 1-3 range.
    ExField.insert_toc_entry(builder, "TC field 4", "A", "5")

    doc.update_fields()
    doc.save(ARTIFACTS_DIR + "Field.tc.docx")

@staticmethod
def insert_toc_entry(builder: aw.DocumentBuilder, text: str, type_identifier: str, entry_level: str):
    """Use a document builder to insert a TC field."""

    field_tc = builder.insert_field(aw.fields.FieldType.FIELD_TOC_ENTRY, True).as_field_tc()
    field_tc.omit_page_number = True
    field_tc.text = text
    field_tc.type_identifier = type_identifier
    field_tc.entry_level = entry_level
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

