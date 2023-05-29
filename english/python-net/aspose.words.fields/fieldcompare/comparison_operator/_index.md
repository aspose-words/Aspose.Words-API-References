---
title: FieldCompare.comparison_operator property
linktitle: comparison_operator property
articleTitle: comparison_operator property
second_title: Aspose.Words for Python
description: "FieldCompare.comparison_operator property. Gets or sets the comparison operator."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldcompare/comparison_operator/
---

## FieldCompare.comparison_operator property

Gets or sets the comparison operator.


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

* module [aspose.words.fields](../../)
* class [FieldCompare](../)

