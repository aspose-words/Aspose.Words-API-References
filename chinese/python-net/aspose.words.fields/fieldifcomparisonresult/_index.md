---
title: FieldIfComparisonResult enumeration
linktitle: FieldIfComparisonResult enumeration
articleTitle: FieldIfComparisonResult enumeration
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldIfComparisonResult enumeration. Specifies the result of the IF field condition evaluation."
type: docs
weight: 550
url: /zh/python-net/aspose.words.fields/fieldifcomparisonresult/
---

## FieldIfComparisonResult enumeration

Specifies the result of the IF field condition evaluation.


### Members

| Name | Description |
| --- | --- |
| ERROR | There is an error in the condition. |
| TRUE | The condition is ``True``. |
| FALSE | The condition is ``False``. |

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
# IF 字段将从其 "TrueText" 属性中显示字符串，
# 或其 "FalseText" 属性，取决于我们构造的语句的真假。
field.true_text = 'True'
field.false_text = 'False'
field.update()
# 在这种情况下，"0 = 1" 不正确，因此显示的结果将是 "False"。
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
# 这次语句正确，因此显示的结果将是 "True"。
self.assertEqual(' IF  5 = "2 + 3" True False', field.get_field_code())
self.assertEqual(aw.fields.FieldIfComparisonResult.TRUE, field.evaluate_condition())
self.assertEqual('True', field.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.IF.docx')
```

### See Also

* module [aspose.words.fields](../)

