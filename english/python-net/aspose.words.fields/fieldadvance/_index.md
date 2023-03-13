﻿---
title: FieldAdvance class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the ADVANCE field"
type: docs
weight: 80
url: /python-net/aspose.words.fields/fieldadvance/
---

## FieldAdvance class

Implements the ADVANCE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Moves the starting point at which the text that lexically follows the field is displayed to the right or left,
up or down, or to a specific horizontal or vertical position.


**Inheritance:** [FieldAdvance](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldAdvance()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [down_offset](./down_offset/) | Gets or sets the number of points by which the text that follows the field should be moved down. |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [horizontal_position](./horizontal_position/) | Gets or sets the number of points by which the text that follows the field should be moved horizontally from the left edge of the column, frame, or text box. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [left_offset](./left_offset/) | Gets or sets the number of points by which the text that follows the field should be moved left. |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [right_offset](./right_offset/) | Gets or sets the number of points by which the text that follows the field should be moved right. |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |
| [up_offset](./up_offset/) | Gets or sets the number of points by which the text that follows the field should be moved up. |
| [vertical_position](./vertical_position/) | Gets or sets the number of points by which the text that follows the field should be moved vertically from the top edge of the page. |

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

Shows how to insert an ADVANCE field, and edit its properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("This text is in its normal place.")

# Below are two ways of using the ADVANCE field to adjust the position of text that follows it.
# The effects of an ADVANCE field continue to be applied until the paragraph ends,
# or another ADVANCE field updates the offset/coordinate values.
# 1 -  Specify a directional offset:
field = builder.insert_field(aw.fields.FieldType.FIELD_ADVANCE, True).as_field_advance()
field.right_offset = "5"
field.up_offset = "5"

self.assertEqual(" ADVANCE  \\r 5 \\u 5", field.get_field_code())

builder.write("This text will be moved up and to the right.")

field = builder.insert_field(aw.fields.FieldType.FIELD_ADVANCE, True).as_field_advance()
field.down_offset = "5"
field.left_offset = "100"

self.assertEqual(" ADVANCE  \\d 5 \\l 100", field.get_field_code())

builder.writeln("This text is moved down and to the left, overlapping the previous text.")

# 2 -  Move text to a position specified by coordinates:
field = builder.insert_field(aw.fields.FieldType.FIELD_ADVANCE, True).as_field_advance()
field.horizontal_position = "-100"
field.vertical_position = "200"

self.assertEqual(" ADVANCE  \\x -100 \\y 200", field.get_field_code())

builder.write("This text is in a custom position.")

doc.save(ARTIFACTS_DIR + "Field.field_advance.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

