---
title: FieldListNum.list_level property
linktitle: list_level property
articleTitle: list_level property
second_title: Aspose.Words for Python
description: "FieldListNum.list_level property. Gets or sets the level in the list, overriding the default behavior of the field."
type: docs
weight: 30
url: /fr/python-net/aspose.words.fields/fieldlistnum/list_level/
---

## FieldListNum.list_level property

Gets or sets the level in the list, overriding the default behavior of the field.


```python
@property
def list_level(self) -> str:
    ...

@list_level.setter
def list_level(self, value: str):
    ...

```

### Examples

Shows how to number paragraphs with LISTNUM fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Les champs LISTNUM affichent un nombre qui s'incrémente à chaque champ LISTNUM.
# Ces champs offrent également une variété d'options qui nous permettent de les utiliser pour émuler des listes numérotées.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
# Les listes commencent à compter à 1 par défaut, mais nous pouvons définir ce nombre à une valeur différente, comme 0.
# Ce champ affichera "0)".
field.starting_number = '0'
builder.writeln('Paragraph 1')
self.assertEqual(' LISTNUM  \\s 0', field.get_field_code())
# Les champs LISTNUM maintiennent des comptes séparés pour chaque niveau de liste.
# Insérer un champ LISTNUM dans le même paragraphe qu'un autre champ LISTNUM
# augmente le niveau de la liste au lieu du compte.
# Le champ suivant continuera le compte que nous avons commencé ci-dessus et affichera une valeur de "1" au niveau de liste 1.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# Ce champ démarrera un compte au niveau de liste 2. Il affichera une valeur de "1".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# Ce champ démarrera un compte au niveau de liste 3. Il affichera une valeur de "1".
# Les différents niveaux de liste ont un formatage différent,
# ainsi ces champs combinés afficheront une valeur de "1)a)i)".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
builder.writeln('Paragraph 2')
# Le prochain champ LISTNUM que nous insérons continuera le comptage au niveau de la liste
# sur lequel le champ LISTNUM précédent était.
# Nous pouvons utiliser la propriété "ListLevel" pour passer à un autre niveau de liste.
# Si ce champ LISTNUM restait au niveau de liste 3, il afficherait "ii)",
# mais, comme nous l'avons déplacé au niveau de liste 2, il poursuit le comptage à ce niveau et affiche "b)".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_level = '2'
builder.writeln('Paragraph 3')
self.assertEqual(' LISTNUM  \\l 2', field.get_field_code())
# Nous pouvons définir la propriété ListName pour que le champ émule un type de champ AUTONUM différent.
# "NumberDefault" émule AUTONUM, "OutlineDefault" émule AUTONUMOUT,
# et "LegalDefault" émule les champs AUTONUMLGL.
# Le nom de liste "OutlineDefault" avec 1 comme numéro de départ affichera "I.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.starting_number = '1'
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 4')
self.assertTrue(field.has_list_name)
self.assertEqual(' LISTNUM  OutlineDefault \\s 1', field.get_field_code())
# Le ListName ne se transmet pas du champ précédent, nous devrons donc le définir pour chaque nouveau champ.
# Ce champ continue le comptage avec le nom de liste différent et affiche "II.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 5')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.LISTNUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldListNum](../)

