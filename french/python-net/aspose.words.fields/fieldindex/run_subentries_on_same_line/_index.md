---
title: FieldIndex.run_subentries_on_same_line property
linktitle: run_subentries_on_same_line property
articleTitle: run_subentries_on_same_line property
second_title: Aspose.Words for Python
description: "FieldIndex.run_subentries_on_same_line property. Gets or sets whether run subentries into the same line as the main entry."
type: docs
weight: 140
url: /fr/python-net/aspose.words.fields/fieldindex/run_subentries_on_same_line/
---

## FieldIndex.run_subentries_on_same_line property

Gets or sets whether run subentries into the same line as the main entry.


```python
@property
def run_subentries_on_same_line(self) -> bool:
    ...

@run_subentries_on_same_line.setter
def run_subentries_on_same_line(self, value: bool):
    ...

```

### Examples

Shows how to work with subentries in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
# Chaque entrée affichera la valeur de la propriété Text du champ XE sur le côté gauche,
# et le numéro de la page contenant le champ XE sur le côté droit.
# L'entrée INDEX collectera tous les champs XE dont les valeurs correspondent dans la propriété \"Text\"
# en une seule entrée plutôt que de créer une entrée pour chaque champ XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.page_number_separator = ', see page '
index.heading = 'A'
# Les champs XE qui ont une propriété Text dont la valeur devient le titre de l'entrée INDEX.
# Si cette valeur contient deux segments de chaîne séparés par un deux‑points (l'entrée INDEX traitera le délimiteur :) ,
# le premier segment est le titre, et le deuxième segment deviendra le sous‑titre.
# Le champ INDEX regroupe d'abord les entrées par ordre alphabétique, puis, s'il y a plusieurs champs XE avec le même
# titres, le champ INDEX les sous‑regroupera davantage selon les valeurs de ces titres.
# Il peut y avoir plusieurs niveaux de sous‑groupement, selon le nombre de fois
# les propriétés Text des champs XE sont segmentées de cette manière.
# Par défaut, un groupe d'entrées de champ INDEX créera une nouvelle ligne pour chaque sous-titre de ce groupe.
# Nous pouvons définir le drapeau RunSubentriesOnSameLine sur true pour conserver le titre,
# et chaque sous-titre du groupe sur une seule ligne à la place, ce qui rendra le champ INDEX plus compact.
index.run_subentries_on_same_line = run_subentries_on_the_same_line
if run_subentries_on_the_same_line:
    self.assertEqual(' INDEX  \\e ", see page " \\h A \\r', index.get_field_code())
else:
    self.assertEqual(' INDEX  \\e ", see page " \\h A', index.get_field_code())
# Insérez deux champs XE, chacun sur une nouvelle page, et avec le même titre nommé "Heading 1",
# que le champ INDEX utilisera pour les regrouper.
# Si RunSubentriesOnSameLine est false, alors le tableau INDEX créera trois lignes:
# une ligne pour le titre de regroupement "Heading 1", et une ligne supplémentaire pour chaque sous-titre.
# Si RunSubentriesOnSameLine est true, alors le tableau INDEX créera une ligne unique
# d'entrée qui englobe le titre et chaque sous-titre.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Heading 1:Subheading 1'
self.assertEqual(' XE  "Heading 1:Subheading 1"', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Heading 1:Subheading 2'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + f'Field.INDEX.XE.Subheading.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

