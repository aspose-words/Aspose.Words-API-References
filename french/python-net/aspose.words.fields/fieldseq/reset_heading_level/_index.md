---
title: FieldSeq.reset_heading_level property
linktitle: reset_heading_level property
articleTitle: reset_heading_level property
second_title: Aspose.Words for Python
description: "FieldSeq.reset_heading_level property. Gets or sets an integer number representing a heading level to reset the sequence number to"
type: docs
weight: 40
url: /fr/python-net/aspose.words.fields/fieldseq/reset_heading_level/
---

## FieldSeq.reset_heading_level property

Gets or sets an integer number representing a heading level to reset the sequence number to.
Returns -1 if the number is absent.


```python
@property
def reset_heading_level(self) -> str:
    ...

@reset_heading_level.setter
def reset_heading_level(self, value: str):
    ...

```

### Examples

Shows create numbering using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Les champs SEQ affichent un compteur qui s'incrémente à chaque champ SEQ.
# Ces champs maintiennent également des compteurs séparés pour chaque séquence nommée unique
# identifiée par la propriété "SequenceIdentifier" du champ SEQ.
# Insérez un champ SEQ qui affichera la valeur du compteur actuel de "MySequence",
# après avoir utilisé la propriété "ResetNumber" pour le définir à 100.
builder.write('#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_number = '100'
field_seq.update()
self.assertEqual(' SEQ  MySequence \\r 100', field_seq.get_field_code())
self.assertEqual('100', field_seq.result)
# Affichez le nombre suivant de cette séquence avec un autre champ SEQ.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.update()
self.assertEqual('101', field_seq.result)
# Insérez un titre de niveau 1.
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('This level 1 heading will reset MySequence to 1')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
# Insérez un autre champ SEQ de la même séquence et configurez-le pour réinitialiser le compteur à chaque titre avec 1.
builder.write('\n#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_heading_level = '1'
field_seq.update()
# Le titre ci‑dessus est un titre de niveau 1, donc le compteur de cette séquence est réinitialisé à 1.
self.assertEqual(' SEQ  MySequence \\s 1', field_seq.get_field_code())
self.assertEqual('1', field_seq.result)
# Passez au nombre suivant de cette séquence.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.insert_next_number = True
field_seq.update()
self.assertEqual(' SEQ  MySequence \\n', field_seq.get_field_code())
self.assertEqual('2', field_seq.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SEQ.ResetNumbering.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSeq](../)

