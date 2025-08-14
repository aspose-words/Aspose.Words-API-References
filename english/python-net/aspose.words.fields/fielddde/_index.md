---
title: FieldDde class
linktitle: FieldDde class
articleTitle: FieldDde class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldDde class. Implements the DDE field"
type: docs
weight: 320
url: /python-net/aspose.words.fields/fielddde/
---

## FieldDde class

Implements the DDE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

For information copied from another application, this field links that information to its original source file using DDE.


**Inheritance:** [FieldDde](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldDde()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [auto_update](./auto_update/) | Gets or sets whether to update this field automatically. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [insert_as_bitmap](./insert_as_bitmap/) | Gets or sets whether to insert the linked object as a bitmap. |
| [insert_as_html](./insert_as_html/) | Gets or sets whether to insert the linked object as HTML format text. |
| [insert_as_picture](./insert_as_picture/) | Gets or sets whether to insert the linked object as a picture. |
| [insert_as_rtf](./insert_as_rtf/) | Gets or sets whether to insert the linked object in rich-text format (RTF). |
| [insert_as_text](./insert_as_text/) | Gets or sets whether to insert the linked object in text-only format. |
| [insert_as_unicode](./insert_as_unicode/) | Gets or sets whether to insert the linked object as Unicode text. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_linked](./is_linked/) | Gets or sets whether to reduce the file size by not storing graphics data with the document. |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [prog_id](./prog_id/) | Gets or sets the application type of the link information. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [source_full_name](./source_full_name/) | Gets or sets the name and location of the source file. |
| [source_item](./source_item/) | Gets or sets the portion of the source file that's being linked. |
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

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

