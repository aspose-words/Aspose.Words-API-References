---
title: FieldIf.comparison_operator property
linktitle: comparison_operator property
articleTitle: comparison_operator property
second_title: Aspose.Words for Python
description: "FieldIf.comparison_operator property. Gets or sets the comparison operator."
type: docs
weight: 20
url: /tr/python-net/aspose.words.fields/fieldif/comparison_operator/
---

## FieldIf.comparison_operator property

Gets or sets the comparison operator.


```python
@property
def comparison_operator(self) -> str:
    ...

@comparison_operator.setter
def comparison_operator(self, value: str):
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
# IF alanı, \"TrueText\" özelliğinden bir dize gösterecektir,
# veya \"FalseText\" özelliğinden, oluşturduğumuz ifadenin doğruluğuna bağlı olarak.
field.true_text = 'True'
field.false_text = 'False'
field.update()
# Bu durumda, \"0 = 1\" yanlıştır, bu yüzden gösterilen sonuç \"False\" olacaktır.
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
# Bu sefer ifade doğrudur, bu yüzden gösterilen sonuç \"True\" olacaktır.
self.assertEqual(' IF  5 = "2 + 3" True False', field.get_field_code())
self.assertEqual(aw.fields.FieldIfComparisonResult.TRUE, field.evaluate_condition())
self.assertEqual('True', field.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.IF.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIf](../)

