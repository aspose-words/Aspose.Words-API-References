﻿---
title: FieldIf.evaluate_condition method
linktitle: evaluate_condition method
articleTitle: evaluate_condition method
second_title: Aspose.Words for Python
description: "FieldIf.evaluate_condition method. Evaluates the condition."
type: docs
weight: 70
url: /python-net/aspose.words.fields/fieldif/evaluate_condition/
---

## evaluate_condition() {#default}

Evaluates the condition.


```python
def evaluate_condition(self):
    ...
```

### Returns

A [FieldIfComparisonResult](../../fieldifcomparisonresult/) value that represents the result of the condition evaluation.



### Examples

Shows how to insert an IF field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Statement 1: ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_IF, update_field=True).as_field_if()
field.left_expression = '0'
field.comparison_operator = '='
field.right_expression = '1'
# The IF field will display a string from either its "TrueText" property,
# or its "FalseText" property, depending on the truth of the statement that we have constructed.
field.true_text = 'True'
field.false_text = 'False'
field.update()
# In this case, "0 = 1" is incorrect, so the displayed result will be "False".
self.assertEqual(' IF  0 = 1 True False', field.get_field_code())
self.assertEqual(aw.fields.FieldIfComparisonResult.FALSE, field.evaluate_condition())
self.assertEqual('False', field.result)
builder.write('\nStatement 2: ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_IF, update_field=True).as_field_if()
field.left_expression = '5'
field.comparison_operator = '='
field.right_expression = '2 + 3'
field.true_text = 'True'
field.false_text = 'False'
field.update()
# This time the statement is correct, so the displayed result will be "True".
self.assertEqual(' IF  5 = "2 + 3" True False', field.get_field_code())
self.assertEqual(aw.fields.FieldIfComparisonResult.TRUE, field.evaluate_condition())
self.assertEqual('True', field.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.IF.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIf](../)

