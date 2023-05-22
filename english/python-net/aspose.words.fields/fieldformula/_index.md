﻿---
title: FieldFormula class
linktitle: FieldFormula class
articleTitle: FieldFormula class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldFormula class. Implements the = (formula) field"
type: docs
weight: 490
url: /python-net/aspose.words.fields/fieldformula/
---

## FieldFormula class

Implements the = (formula) field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Calcualtes the result of an expression.


**Inheritance:** [FieldFormula](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldFormula()](./__init__/#default) | The default constructor. |

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

Shows how to use the formula field to display the result of an equation.

```python
doc = aw.Document()

# Use a field builder to construct a mathematical equation,
# then create a formula field to display the equation's result in the document.
field_builder = aw.fields.FieldBuilder(aw.fields.FieldType.FIELD_FORMULA)
field_builder.add_argument(2)
field_builder.add_argument("*")
field_builder.add_argument(5)

field = field_builder.build_and_insert(doc.first_section.body.first_paragraph).as_field_formula()
field.update()

self.assertEqual(" = 2 * 5 ", field.get_field_code())
self.assertEqual("10", field.result)

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_formula.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

