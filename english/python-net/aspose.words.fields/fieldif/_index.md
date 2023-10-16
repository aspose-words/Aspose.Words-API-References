---
title: FieldIf class
linktitle: FieldIf class
articleTitle: FieldIf class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldIf class. Implements the IF field"
type: docs
weight: 540
url: /python-net/aspose.words.fields/fieldif/
---

## FieldIf class

Implements the IF field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Compares the values designated by the expressions [FieldIf.left_expression](./left_expression/) and [FieldIf.right_expression](./right_expression/)
in comparison using the operator designated by [FieldIf.comparison_operator](./comparison_operator/).

A field in the following format will be used as a mail merge source: { IF 0 = 0 "{PatientsNameFML}" "" \\\* MERGEFORMAT }




**Inheritance:** [FieldIf](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldIf()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [comparison_operator](./comparison_operator/) | Gets or sets the comparison operator. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [false_text](./false_text/) | Gets or sets the text displayed if the comparison expression is ``False``. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [left_expression](./left_expression/) | Gets or sets the left part of the comparison expression. |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [right_expression](./right_expression/) | Gets or sets the right part of the comparison expression. |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [true_text](./true_text/) | Gets or sets the text displayed if the comparison expression is true. |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ evaluate_condition()](./evaluate_condition/#default) | Evaluates the condition. |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### Examples

Shows how to insert an IF field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("Statement 1: ")
field = builder.insert_field(aw.fields.FieldType.FIELD_IF, True).as_field_if()
field.left_expression = "0"
field.comparison_operator = "="
field.right_expression = "1"

# The IF field will display a string from either its "true_text" property,
# or its "false_text" property, depending on the truth of the statement that we have constructed.
field.true_text = "True"
field.false_text = "False"
field.update()

# In this case, "0 = 1" is incorrect, so the displayed result will be "False".
self.assertEqual(" IF  0 = 1 True False", field.get_field_code())
self.assertEqual(aw.fields.FieldIfComparisonResult.FALSE, field.evaluate_condition())
self.assertEqual("False", field.result)

builder.write("\nStatement 2: ")
field = builder.insert_field(aw.fields.FieldType.FIELD_IF, True).as_field_if()
field.left_expression = "5"
field.comparison_operator = "="
field.right_expression = "2 + 3"
field.true_text = "True"
field.false_text = "False"
field.update()

# This time the statement is correct, so the displayed result will be "True".
self.assertEqual(" IF  5 = \"2 + 3\" True False", field.get_field_code())
self.assertEqual(aw.fields.FieldIfComparisonResult.TRUE, field.evaluate_condition())
self.assertEqual("True", field.result)

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_if.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

