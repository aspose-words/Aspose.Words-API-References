---
title: FieldTime class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the TIME field"
type: docs
weight: 1040
url: /python-net/aspose.words.fields/fieldtime/
---

## FieldTime class

Implements the TIME field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.




Inserts the current date and time.


**Inheritance:** [FieldTime](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldTime()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
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

Shows how to display the current time using the TIME field.

```python
def test_field_time(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    # By default, time is displayed in the "h:mm am/pm" format.
    field = ExField.insert_field_time(builder, "")

    self.assertEqual(" TIME ", field.get_field_code())

    # We can use the \@ flag to change the format of our displayed time.
    field = ExField.insert_field_time(builder, "\\@ HHmm")

    self.assertEqual(" TIME \\@ HHmm", field.get_field_code())

    # We can adjust the format to get TIME field to also display the date, according to the Gregorian calendar.
    field = ExField.insert_field_time(builder, "\\@ \"M/d/yyyy h mm:ss am/pm\"")

    self.assertEqual(" TIME \\@ \"M/d/yyyy h mm:ss am/pm\"", field.get_field_code())

    doc.save(ARTIFACTS_DIR + "Field.field_time.docx")

@staticmethod
def insert_field_time(builder: aw.DocumentBuilder, format: str) -> aw.fields.FieldTime:
    """Use a document builder to insert a TIME field, insert a new paragraph and return the field."""

    field = builder.insert_field(aw.fields.FieldType.FIELD_TIME, True).as_field_time()
    builder.move_to(field.separator)
    builder.write(format)
    builder.move_to(field.start.parent_node)

    builder.insert_paragraph()
    return field
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

