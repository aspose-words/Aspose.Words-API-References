﻿---
title: FieldCompare class
linktitle: FieldCompare class
articleTitle: FieldCompare class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldCompare class. Implements the COMPARE field"
type: docs
weight: 250
url: /python-net/aspose.words.fields/fieldcompare/
---

## FieldCompare class

Implements the COMPARE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Compares the values designated by the expressions [FieldCompare.left_expression](./left_expression/) and [FieldCompare.right_expression](./right_expression/)
in comparison using the operator designated by [FieldCompare.comparison_operator](./comparison_operator/).



**Inheritance:** [FieldCompare](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldCompare()](./__init__/#default) | The default constructor. |

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

Shows how to compare expressions using a COMPARE field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

field = builder.insert_field(aw.fields.FieldType.FIELD_COMPARE, True).as_field_compare()
field.left_expression = "3"
field.comparison_operator = "<"
field.right_expression = "2"
field.update()

# The COMPARE field displays a "0" or a "1", depending on its statement's truth.
# The result of this statement is False so that this field will display a "0".
self.assertEqual(" COMPARE  3 < 2", field.get_field_code())
self.assertEqual("0", field.result)

builder.writeln()

field = builder.insert_field(aw.fields.FieldType.FIELD_COMPARE, True).as_field_compare()
field.left_expression = "5"
field.comparison_operator = "="
field.right_expression = "2 + 3"
field.update()

# This field displays a "1" since the statement is True.
self.assertEqual(" COMPARE  5 = \"2 + 3\"", field.get_field_code())
self.assertEqual("1", field.result)

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_compare.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

