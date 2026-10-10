---
title: FieldCompare.right_expression property
linktitle: right_expression property
articleTitle: right_expression property
second_title: Aspose.Words for Python
description: "FieldCompare.right_expression property. Gets or sets the right part of the comparison expression."
type: docs
weight: 40
url: /ar/python-net/aspose.words.fields/fieldcompare/right_expression/
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
# يعرض حقل COMPARE "0" أو "1"، اعتمادًا على صحة بيانه.
# نتيجة هذا البيان هي false لذا سيعرض هذا الحقل "0".
self.assertEqual(' COMPARE  3 < 2', field.get_field_code())
self.assertEqual('0', field.result)
builder.writeln()
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMPARE, update_field=True).as_field_compare()
field.left_expression = '5'
field.comparison_operator = '='
field.right_expression = '2 + 3'
field.update()
# يعرض هذا الحقل "1" لأن البيان صحيح.
self.assertEqual(' COMPARE  5 = "2 + 3"', field.get_field_code())
self.assertEqual('1', field.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.COMPARE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldCompare](../)

