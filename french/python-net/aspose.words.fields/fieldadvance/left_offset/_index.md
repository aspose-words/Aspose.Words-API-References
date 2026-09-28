---
title: FieldAdvance.left_offset property
linktitle: left_offset property
articleTitle: left_offset property
second_title: Aspose.Words for Python
description: "FieldAdvance.left_offset property. Gets or sets the number of points by which the text that follows the field should be moved left."
type: docs
weight: 40
url: /fr/python-net/aspose.words.fields/fieldadvance/left_offset/
---

## FieldAdvance.left_offset property

Gets or sets the number of points by which the text that follows the field should be moved left.


```python
@property
def left_offset(self) -> str:
    ...

@left_offset.setter
def left_offset(self, value: str):
    ...

```

### Examples

Shows how to insert an ADVANCE field, and edit its properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('This text is in its normal place.')
# Voici deux façons d'utiliser le champ ADVANCE pour ajuster la position du texte qui le suit.
# Les effets d'un champ ADVANCE continuent d'être appliqués jusqu'à la fin du paragraphe,
# ou qu'un autre champ ADVANCE mette à jour les valeurs de décalage/coordonnées.
# 1 -  Spécifier un décalage directionnel :
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
# 2 -  Déplacer le texte vers une position spécifiée par des coordonnées :
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

