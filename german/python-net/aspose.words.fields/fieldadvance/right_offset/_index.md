---
title: FieldAdvance.right_offset property
linktitle: right_offset property
articleTitle: right_offset property
second_title: Aspose.Words for Python
description: "FieldAdvance.right_offset property. Gets or sets the number of points by which the text that follows the field should be moved right."
type: docs
weight: 50
url: /de/python-net/aspose.words.fields/fieldadvance/right_offset/
---

## FieldAdvance.right_offset property

Gets or sets the number of points by which the text that follows the field should be moved right.


```python
@property
def right_offset(self) -> str:
    ...

@right_offset.setter
def right_offset(self, value: str):
    ...

```

### Examples

Shows how to insert an ADVANCE field, and edit its properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('This text is in its normal place.')
# Unten sind zwei Möglichkeiten, das ADVANCE-Feld zu verwenden, um die Position des nachfolgenden Textes anzupassen.
# Die Effekte eines ADVANCE-Feldes werden weiter angewendet, bis der Absatz endet,
# oder ein weiteres ADVANCE-Feld die Versatz-/Koordinatenwerte aktualisiert.
# 1 -  Einen Richtungsversatz angeben:
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
# 2 -  Text an eine durch Koordinaten angegebene Position verschieben:
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

