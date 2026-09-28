---
title: FieldCompare.right_expression property
linktitle: right_expression property
articleTitle: right_expression property
second_title: Aspose.Words for Python
description: "FieldCompare.right_expression property. Gets or sets the right part of the comparison expression."
type: docs
weight: 40
url: /zh/python-net/aspose.words.fields/fieldcompare/right_expression/
---

## FieldCompare.right_expression property

Gets or sets the right part of the comparison expression.


```python
@property
def right_expression(self) -> str:
    ...

@right_expression.setter
def right_expression(self, value: str):
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
# COMPARE 字段显示 "0" 或 "1"，取决于其语句的真假。
# 此语句的结果为 false，因此该字段将显示 "0"。
self.assertEqual(' COMPARE  3 < 2', field.get_field_code())
self.assertEqual('0', field.result)
builder.writeln()
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMPARE, update_field=True).as_field_compare()
field.left_expression = '5'
field.comparison_operator = '='
field.right_expression = '2 + 3'
field.update()
# 由于语句为 true，此字段显示 "1"。
self.assertEqual(' COMPARE  5 = "2 + 3"', field.get_field_code())
self.assertEqual('1', field.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.COMPARE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldCompare](../)

