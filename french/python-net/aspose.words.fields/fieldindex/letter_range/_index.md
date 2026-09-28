---
title: FieldIndex.letter_range property
linktitle: letter_range property
articleTitle: letter_range property
second_title: Aspose.Words for Python
description: "FieldIndex.letter_range property. Gets or sets a range of letters to which limit the index."
type: docs
weight: 90
url: /fr/python-net/aspose.words.fields/fieldindex/letter_range/
---

## FieldIndex.letter_range property

Gets or sets a range of letters to which limit the index.


```python
@property
def letter_range(self) -> str:
    ...

@letter_range.setter
def letter_range(self, value: str):
    ...

```

### Examples

Shows how to populate an INDEX field with entries using XE fields, and also modify its appearance.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
# Chaque entrée affichera la valeur de la propriété Text du champ XE sur le côté gauche,
# et le numéro de la page contenant le champ XE sur le côté droit.
# Si les champs XE ont la même valeur dans leur propriété "Text",
# le champ INDEX les regroupera en une seule entrée.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.language_id = '1033'
# Définir la valeur de cette propriété à "A" regroupera toutes les entrées par leur première lettre,
# et placera cette lettre en majuscule au-dessus de chaque groupe.
index.heading = 'A'
# Définissez le tableau créé par le champ INDEX pour qu'il s'étende sur 2 colonnes.
index.number_of_columns = '2'
# Définissez que toute entrée dont la lettre de départ se trouve en dehors de la plage de caractères "a-c" soit omise.
index.letter_range = 'a-c'
self.assertEqual(' INDEX  \\z 1033 \\h A \\c 2 \\p a-c', index.get_field_code())
# Les deux prochains champs XE apparaîtront sous le titre "A",
# avec leurs styles de texte respectifs également appliqués à leurs numéros de page.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apple'
index_entry.is_italic = True
self.assertEqual(' XE  Apple \\i', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apricot'
index_entry.is_bold = True
self.assertEqual(' XE  Apricot \\b', index_entry.get_field_code())
# Les deux prochains champs XE seront sous les titres "B" et "C" dans la table des matières des champs INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Banana'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cherry'
# Les champs INDEX trient toutes les entrées par ordre alphabétique, ainsi cette entrée apparaîtra sous "A" avec les deux autres.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Avocado'
# Cette entrée n'apparaîtra pas car elle commence par la lettre "D",
# qui se trouve en dehors de la plage de caractères "a-c" définie par la propriété LetterRange du champ INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Durian'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Formatting.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

