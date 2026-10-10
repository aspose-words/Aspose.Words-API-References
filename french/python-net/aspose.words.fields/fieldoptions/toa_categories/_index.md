---
title: FieldOptions.toa_categories property
linktitle: toa_categories property
articleTitle: toa_categories property
second_title: Aspose.Words for Python
description: "FieldOptions.toa_categories property. Gets or sets the table of authorities categories."
type: docs
weight: 190
url: /fr/python-net/aspose.words.fields/fieldoptions/toa_categories/
---

## FieldOptions.toa_categories property

Gets or sets the table of authorities categories.


```python
@property
def toa_categories(self) -> aspose.words.fields.ToaCategories:
    ...

@toa_categories.setter
def toa_categories(self, value: aspose.words.fields.ToaCategories):
    ...

```

### Examples

Shows how to specify a set of categories for TOA fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Les champs TOA peuvent filtrer leurs entrées par catégories définies dans cette collection.
toa_categories = aw.fields.ToaCategories()
doc.field_options.toa_categories = toa_categories
# Cette collection de catégories comprend des valeurs par défaut, que nous pouvons remplacer par des valeurs personnalisées.
self.assertEqual('Cases', toa_categories[1])
self.assertEqual('Statutes', toa_categories[2])
toa_categories[1] = 'My Category 1'
toa_categories[2] = 'My Category 2'
# Nous pouvons toujours accéder aux valeurs par défaut via cette collection.
self.assertEqual('Cases', aw.fields.ToaCategories.default_categories[1])
self.assertEqual('Statutes', aw.fields.ToaCategories.default_categories[2])
# Insérez 2 champs TOA. Les champs TOA créent une entrée pour chaque champ TA dans le document.
# Utilisez le commutateur "\c" pour sélectionner l'index d'une catégorie de notre collection.
#  Avec ce commutateur, un champ TOA ne récupérera que les entrées des champs TA qui
# ont également un commutateur "\c" avec un index de catégorie correspondant. Chaque champ TOA affichera également
# le nom de la catégorie vers laquelle son commutateur "\c" pointe.
builder.insert_field(field_code='TOA \\c 1 \\h', field_value=None)
builder.insert_field(field_code='TOA \\c 2 \\h', field_value=None)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Insérez des entrées TOA dans 2 catégories. Notre premier champ TOA recevra une entrée,
# du deuxième champ TA dont le commutateur "\c" pointe également vers la première catégorie.
# Le deuxième champ TOA aura deux entrées provenant des deux autres champs TA.
builder.insert_field(field_code='TA \\c 2 \\l "entry 1"')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_field(field_code='TA \\c 1 \\l "entry 2"')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_field(field_code='TA \\c 2 \\l "entry 3"')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'FieldOptions.TOA.Categories.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

