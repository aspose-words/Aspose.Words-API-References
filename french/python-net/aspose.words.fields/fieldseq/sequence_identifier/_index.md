---
title: FieldSeq.sequence_identifier property
linktitle: sequence_identifier property
articleTitle: sequence_identifier property
second_title: Aspose.Words for Python
description: "FieldSeq.sequence_identifier property. Gets or sets the name assigned to the series of items that are to be numbered."
type: docs
weight: 60
url: /fr/python-net/aspose.words.fields/fieldseq/sequence_identifier/
---

## FieldSeq.sequence_identifier property

Gets or sets the name assigned to the series of items that are to be numbered.


```python
@property
def sequence_identifier(self) -> str:
    ...

@sequence_identifier.setter
def sequence_identifier(self, value: str):
    ...

```

### Examples

Shows how to populate a TOC field with entries using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Un champ TOC peut créer une entrée dans sa table des matières pour chaque champ SEQ trouvé dans le document.
# Chaque entrée contient le paragraphe qui inclut le champ SEQ ainsi que le numéro de page où le champ apparaît.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Les champs SEQ affichent un compteur qui s'incrémente à chaque champ SEQ.
# Ces champs maintiennent également des compteurs séparés pour chaque séquence nommée unique
# identifiée par la propriété "SequenceIdentifier" du champ SEQ.
# Utilisez la propriété "TableOfFiguresLabel" pour nommer une séquence principale pour le TOC.
# Désormais, ce TOC ne créera des entrées qu'à partir des champs SEQ dont le "SequenceIdentifier" est défini sur "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# Nous pouvons nommer une autre séquence de champ SEQ dans la propriété "PrefixedSequenceIdentifier".
# Les champs SEQ de cette séquence préfixée ne créeront pas d'entrées TOC.
# Chaque entrée TOC créée à partir d'un champ SEQ de séquence principale affichera désormais également le compteur qui
# la séquence de préfixe est actuellement sur le champ SEQ de séquence principale qui a créé l'entrée.
field_toc.prefixed_sequence_identifier = 'PrefixSequence'
# Chaque entrée du TOC affichera le compteur de séquence de préfixe immédiatement à gauche
# du numéro de page sur lequel le champ SEQ de séquence principale apparaît.
# Nous pouvons spécifier un séparateur personnalisé qui apparaîtra entre ces deux nombres.
field_toc.sequence_separator = '>'
self.assertEqual(' TOC  \\c MySequence \\s PrefixSequence \\d >', field_toc.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Il existe deux façons d'utiliser les champs SEQ pour remplir ce TOC.
# 1 - Insertion d'un champ SEQ qui appartient à la séquence de préfixe du TOC :
# Ce champ incrémentera le compteur de séquence SEQ pour le "PrefixSequence" de 1.
# Puisque ce champ n'appartient pas à la séquence principale identifiée
# par la propriété "TableOfFiguresLabel" du TOC, il n'apparaîtra pas comme une entrée.
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
self.assertEqual(' SEQ  PrefixSequence', field_seq.get_field_code())
# 2 - Insertion d'un champ SEQ qui appartient à la séquence principale du TOC :
# Ce champ SEQ créera une entrée dans le TOC.
# L'entrée du TOC contiendra le paragraphe dans lequel se trouve le champ SEQ ainsi que le numéro de la page où il apparaît.
# Cette entrée affichera également le compteur actuel de la séquence de préfixe,
# séparé du numéro de page par la valeur de la propriété SeqenceSeparator du TOC.
# Le compteur "PrefixSequence" est à 1, ce champ SEQ de séquence principale est à la page 2,
# et le séparateur est ">", donc l'entrée affichera "1>2".
builder.write('First TOC entry, MySequence #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', field_seq.get_field_code())
# Insérez une page, avancez la séquence de préfixe de 2, puis insérez un champ SEQ pour créer une entrée TOC ensuite.
# La séquence de préfixe est maintenant à 2, et le champ SEQ de séquence principale est à la page 3,
# ainsi l'entrée du TOC affichera "2>3" dans son compteur de page.
builder.insert_break(aw.BreakType.PAGE_BREAK)
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
builder.write('Second TOC entry, MySequence #')
field_seq.sequence_identifier = 'MySequence'
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOC.SEQ.docx')
```

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

