﻿---
title: FieldEditTime class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the EDITTIME field"
type: docs
weight: 380
url: /python-net/aspose.words.fields/fieldedittime/
---

## FieldEditTime class

Implements the EDITTIME field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Retrieves the total editing time, in minutes, since the document was created.


**Inheritance:** [FieldEditTime](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldEditTime()](./__init__/#default) | The default constructor. |

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

Shows how to use the EDITTIME field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# The EDITTIME field will show, in minutes,
# the time spent with the document open in a Microsoft Word window.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write("You've been editing this document for ")
field = builder.insert_field(aw.fields.FieldType.FIELD_EDIT_TIME, True).as_field_edit_time()
builder.writeln(" minutes.")

# This built in document property tracks the minutes. Microsoft Word uses this property
# to track the time spent with the document open. We can also edit it ourselves.
doc.built_in_document_properties.total_editing_time = 10
field.update()

self.assertEqual(" EDITTIME ", field.get_field_code())
self.assertEqual("10", field.result)

# The field does not update itself in real-time, and will also have to be
# manually updated in Microsoft Word anytime we need an accurate value.
doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_edit_time.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

