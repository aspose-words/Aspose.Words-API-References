---
title: FieldCompare.left_expression property
linktitle: left_expression property
articleTitle: left_expression property
second_title: Aspose.Words for Python
description: "FieldCompare.left_expression property. Gets or sets the left part of the comparison expression."
type: docs
weight: 30
url: /python-net/aspose.words.fields/fieldcompare/left_expression/
---

## FieldCompare.left_expression property

Gets or sets the left part of the comparison expression.


```python
@property
def left_expression(self) -> str:
    ...

@left_expression.setter
def left_expression(self, value: str):
    ...

```

### Examples

Shows how to compare expressions using a COMPARE field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMPARE, update_field=True).as_field_compare()
field.left_expression = '3'
field.comparison_operator = '<'
field.right_expression = '2'
field.update()
# The COMPARE field displays a "0" or a "1", depending on its statement's truth.
# The result of this statement is false so that this field will display a "0".
self.assertEqual(' COMPARE  3 < 2', field.get_field_code())
self.assertEqual('0', field.result)
builder.writeln()
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMPARE, update_field=True).as_field_compare()
field.left_expression = '5'
field.comparison_operator = '='
field.right_expression = '2 + 3'
field.update()
# This field displays a "1" since the statement is true.
self.assertEqual(' COMPARE  5 = "2 + 3"', field.get_field_code())
self.assertEqual('1', field.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.COMPARE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldCompare](../)

