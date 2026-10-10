---
title: FieldCompare.right_expression property
linktitle: right_expression property
articleTitle: right_expression property
second_title: Aspose.Words for Python
description: "FieldCompare.right_expression property. Gets or sets the right part of the comparison expression."
type: docs
weight: 40
url: /it/python-net/aspose.words.fields/fieldcompare/right_expression/
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
# Il campo COMPARE visualizza un "0" o un "1", a seconda della verità della sua affermazione.
# Il risultato di questa affermazione è falso, quindi questo campo visualizzerà un "0".
self.assertEqual(' COMPARE  3 < 2', field.get_field_code())
self.assertEqual('0', field.result)
builder.writeln()
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMPARE, update_field=True).as_field_compare()
field.left_expression = '5'
field.comparison_operator = '='
field.right_expression = '2 + 3'
field.update()
# Questo campo visualizza un "1" poiché l'affermazione è vera.
self.assertEqual(' COMPARE  5 = "2 + 3"', field.get_field_code())
self.assertEqual('1', field.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.COMPARE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldCompare](../)

