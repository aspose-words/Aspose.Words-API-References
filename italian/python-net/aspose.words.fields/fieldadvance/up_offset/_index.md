---
title: FieldAdvance.up_offset property
linktitle: up_offset property
articleTitle: up_offset property
second_title: Aspose.Words for Python
description: "FieldAdvance.up_offset property. Gets or sets the number of points by which the text that follows the field should be moved up."
type: docs
weight: 60
url: /it/python-net/aspose.words.fields/fieldadvance/up_offset/
---

## FieldAdvance.up_offset property

Gets or sets the number of points by which the text that follows the field should be moved up.


```python
@property
def up_offset(self) -> str:
    ...

@up_offset.setter
def up_offset(self, value: str):
    ...

```

### Examples

Shows how to insert an ADVANCE field, and edit its properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('This text is in its normal place.')
# Di seguito sono riportati due modi per usare il campo ADVANCE per regolare la posizione del testo che lo segue.
# Gli effetti di un campo ADVANCE continuano ad essere applicati fino alla fine del paragrafo,
# o un altro campo ADVANCE aggiorna i valori di offset/coordinate.
# 1 -  Specifica un offset direzionale:
field = builder.insert_field(aw.fields.FieldType.FIELD_ADVANCE, True).as_field_advance()
field.right_offset = '5'
field.up_offset = '5'
self.assertEqual(' ADVANCE  \\r 5 \\u 5', field.get_field_code())
builder.write('This text will be moved up and to the right.')
field = builder.insert_field(aw.fields.FieldType.FIELD_ADVANCE, True).as_field_advance()
field.down_offset = '5'
field.left_offset = '100'
self.assertEqual(' ADVANCE  \\d 5 \\l 100', field.get_field_code())
builder.writeln('This text is moved down and to the left, overlapping the previous text.')
# 2 -  Sposta il testo a una posizione specificata dalle coordinate:
field = builder.insert_field(aw.fields.FieldType.FIELD_ADVANCE, True).as_field_advance()
field.horizontal_position = '-100'
field.vertical_position = '200'
self.assertEqual(' ADVANCE  \\x -100 \\y 200', field.get_field_code())
builder.write('This text is in a custom position.')
doc.save(ARTIFACTS_DIR + 'Field.field_advance.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAdvance](../)

