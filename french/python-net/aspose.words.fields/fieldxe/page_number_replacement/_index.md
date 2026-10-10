---
title: FieldXE.page_number_replacement property
linktitle: page_number_replacement property
articleTitle: page_number_replacement property
second_title: Aspose.Words for Python
description: "FieldXE.page_number_replacement property. Gets or sets text used in place of a page number."
type: docs
weight: 50
url: /fr/python-net/aspose.words.fields/fieldxe/page_number_replacement/
---

## FieldXE.page_number_replacement property

Gets or sets text used in place of a page number.


```python
@property
def page_number_replacement(self) -> str:
    ...

@page_number_replacement.setter
def page_number_replacement(self, value: str):
    ...

```

### Examples

Shows how to define cross references in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
# Chaque entrée affichera la valeur de la propriété Text du champ XE sur le côté gauche,
# et le numéro de la page contenant le champ XE sur le côté droit.
# L'entrée INDEX collectera tous les champs XE dont les valeurs correspondent dans la propriété \"Text\"
# en une seule entrée plutôt que de créer une entrée pour chaque champ XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Nous pouvons configurer un champ XE pour que son entrée INDEX affiche une chaîne au lieu d'un numéro de page.
# Tout d'abord, pour les entrées qui remplacent un numéro de page par une chaîne,
# spécifiez un séparateur personnalisé entre la valeur de la propriété Text du champ XE et la chaîne.
index.cross_reference_separator = ', see: '
self.assertEqual(' INDEX  \\k ", see: "', index.get_field_code())
# Insérez un champ XE, qui crée une entrée INDEX normale affichant le numéro de page de ce champ,
# et n'invoque pas la valeur CrossReferenceSeparator.
# L'entrée de ce champ XE affichera \"Apple, 2\".
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apple'
self.assertEqual(' XE  Apple', index_entry.get_field_code())
# Insérez un autre champ XE à la page 3 et définissez une valeur pour la propriété PageNumberReplacement.
# Cette valeur apparaîtra à la place du numéro de la page sur laquelle se trouve ce champ,
# et la valeur CrossReferenceSeparator du champ INDEX apparaîtra devant elle.
# L'entrée de ce champ XE affichera \"Banane, voir : Fruit tropical\".
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Banana'
index_entry.page_number_replacement = 'Tropical fruit'
self.assertEqual(' XE  Banana \\t "Tropical fruit"', index_entry.get_field_code())
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.CrossReferenceSeparator.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldXE](../)

