---
title: FieldIf.true_text property
linktitle: true_text property
articleTitle: true_text property
second_title: Aspose.Words for Python
description: "FieldIf.true_text property. Gets or sets the text displayed if the comparison expression is true."
type: docs
weight: 60
url: /es/python-net/aspose.words.fields/fieldif/true_text/
---

## FieldIf.true_text property

Gets or sets the text displayed if the comparison expression is true.


```python
@property
def true_text(self) -> str:
    ...

@true_text.setter
def true_text(self, value: str):
    ...

```

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
# El campo IF mostrará una cadena de su propiedad "TrueText",
# o de su propiedad "FalseText", dependiendo de la veracidad de la declaración que hemos construido.
field.true_text = 'True'
field.false_text = 'False'
field.update()
# En este caso, "0 = 1" es incorrecto, por lo que el resultado mostrado será "False".
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
# Esta vez la declaración es correcta, por lo que el resultado mostrado será "True".
self.assertEqual(' IF  5 = "2 + 3" True False', field.get_field_code())
self.assertEqual(aw.fields.FieldIfComparisonResult.TRUE, field.evaluate_condition())
self.assertEqual('True', field.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.IF.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIf](../)

