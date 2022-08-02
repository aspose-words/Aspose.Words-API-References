---
title: FieldMergeField class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the MERGEFIELD field."
type: docs
weight: 690
url: /python-net/aspose.words.fields/fieldmergefield/
---

## FieldMergeField class

Implements the MERGEFIELD field.


Retrieves the name of a data field within the merge characters in a mail merge main document.
When the main document is merged with the selected data source, information from the specified
data field is inserted in place of the merge field.


**Inheritance:** [FieldMergeField](./) → [Field](../field/)

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [field_name](./field_name/) | Gets or sets the name of a data field. |
| [field_name_no_prefix](./field_name_no_prefix/) | Returns just the name of the data field. Any prefix is stripped to the prefix property. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [is_mapped](./is_mapped/) | Gets or sets whether this field is a mapped field. |
| [is_vertical_formatting](./is_vertical_formatting/) | Gets or sets whether to enable character conversion for vertical formatting. |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be null.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [text_after](./text_after/) | Gets or sets the text to be inserted after the field if the field is not blank. |
| [text_before](./text_before/) | Gets or sets the text to be inserted before the field if the field is not blank. |
| [type](./type/) | Gets the Microsoft Word field type. |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

