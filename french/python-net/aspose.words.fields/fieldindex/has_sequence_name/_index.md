---
title: FieldIndex.has_sequence_name property
linktitle: has_sequence_name property
articleTitle: has_sequence_name property
second_title: Aspose.Words for Python
description: "FieldIndex.has_sequence_name property. Gets a value indicating whether a sequence should be used while the field's result building."
type: docs
weight: 60
url: /fr/python-net/aspose.words.fields/fieldindex/has_sequence_name/
---

## FieldIndex.has_sequence_name property

Gets a value indicating whether a sequence should be used while the field's result building.


```python
@property
def has_sequence_name(self) -> bool:
    ...

```

### Examples

Shows how to split a document into portions by combining INDEX and SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
# Chaque entrée affichera la valeur de la propriété Text du champ XE sur le côté gauche,
# et le numéro de la page contenant le champ XE sur le côté droit.
# Si les champs XE ont la même valeur dans leur propriété "Text",
# le champ INDEX les regroupera en une seule entrée.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Dans la propriété SequenceName, nommez une séquence de champ SEQ. Chaque entrée de ce champ INDEX affichera désormais également
# le numéro auquel le compteur de séquence se trouve à l'emplacement du champ XE qui a créé cette entrée.
index.sequence_name = 'MySequence'
# Définissez le texte qui entourera la séquence et les numéros de page pour expliquer leur signification à l'utilisateur.
# Une entrée créée avec cette configuration affichera quelque chose comme "MySequence à 1 sur la page 1" à son numéro de page.
# PageNumberSeparator et SequenceSeparator ne peuvent pas dépasser 15 caractères.
index.page_number_separator = '\tMySequence at '
index.sequence_separator = ' on page '
self.assertTrue(index.has_sequence_name)
self.assertEqual(' INDEX  \\s MySequence \\e "\tMySequence at " \\d " on page "', index.get_field_code())
# Les champs SEQ affichent un compteur qui s'incrémente à chaque champ SEQ.
# Ces champs maintiennent également des compteurs séparés pour chaque séquence nommée unique
# identifiée par la propriété "SequenceIdentifier" du champ SEQ.
# Insérez un champ SEQ qui déplace la séquence "MySequence" à 1.
# Ce champ n'est pas différent du texte normal du document. Il n'apparaîtra pas dans la table des matières d'un champ INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', sequence_field.get_field_code())
# Insérez un champ XE qui créera une entrée dans le champ INDEX.
# Puisque "MySequence" est à 1 et que ce champ XE se trouve à la page 2, avec les séparateurs personnalisés que nous avons définis ci‑dessus,
# l'entrée INDEX de ce champ affichera "Cat" sur le côté gauche, et "MySequence à 1 sur la page 2" sur le côté droit.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
self.assertEqual(' XE  Cat', index_entry.get_field_code())
# Insérez un saut de page et utilisez des champs SEQ pour faire passer "MySequence" à 3.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
# Insérez un champ XE avec la même propriété Text que celui ci‑dessus.
# L'entrée INDEX regroupera les champs XE avec des valeurs correspondantes dans la propriété "Text"
# en une seule entrée plutôt que de créer une entrée pour chaque champ XE.
# Comme nous sommes à la page 2 avec "MySequence" à 3, ", 3 sur la page 3" sera ajouté à la même entrée INDEX que ci‑dessus.
# La partie numéro de page de cette entrée INDEX affichera désormais "MySequence à 1 sur la page 2, 3 sur la page 3".
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
# Insérez un champ XE avec une nouvelle valeur de propriété Text unique.
# Cela ajoutera une nouvelle entrée, avec MySequence à 3 sur la page 4.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Dog'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Sequence.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

