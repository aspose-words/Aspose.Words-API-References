---
title: FieldNextIf class
linktitle: FieldNextIf class
articleTitle: FieldNextIf class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldNextIf class. Implements the NEXTIF field"
type: docs
weight: 730
url: /python-net/aspose.words.fields/fieldnextif/
---

## FieldNextIf class

Implements the NEXTIF field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Compares the values designated by the expressions [FieldNextIf.left_expression](./left_expression/) and [FieldNextIf.right_expression](./right_expression/)
in comparison using the operator designated by [FieldNextIf.comparison_operator](./comparison_operator/). If the comparison is true,
the next data record is merged into the current merge document. (Merge fields that follow the NEXTIF in the main
document are replaced by values from the next data record rather than the current data record.)
If the comparison is false, the next data record is merged into a new merge document.



**Inheritance:** [FieldNextIf](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldNextIf()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [comparison_operator](./comparison_operator/) | Gets or sets the comparison operator. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [left_expression](./left_expression/) | Gets or sets the left part of the comparison expression. |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [right_expression](./right_expression/) | Gets or sets the right part of the comparison expression. |
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

Shows how to use NEXT/NEXTIF fields to merge multiple rows into one page during a mail merge (InsertMergeFields).

```python
def insert_merge_fields(self, builder, first_field_text_before):
    self.insert_merge_field(builder, 'Courtesy Title', first_field_text_before, ' ')
    self.insert_merge_field(builder, 'First Name', None, ' ')
    self.insert_merge_field(builder, 'Last Name', None, None)
    builder.insert_paragraph()

def insert_merge_field(self, builder, field_name, text_before, text_after):
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_MERGE_FIELD, update_field=True).as_field_merge_field()
    field.field_name = field_name
    field.text_before = text_before
    field.text_after = text_after
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

