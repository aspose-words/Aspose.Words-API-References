---
title: FieldAutoNum.separator_character property
linktitle: separator_character property
articleTitle: separator_character property
second_title: Aspose.Words for Python
description: "FieldAutoNum.separator_character property. Gets or sets the separator character to be used."
type: docs
weight: 20
url: /fr/python-net/aspose.words.fields/fieldautonum/separator_character/
---

## FieldAutoNum.separator_character property

Gets or sets the separator character to be used.


```python
@property
def separator_character(self) -> str:
    ...

@separator_character.setter
def separator_character(self, value: str):
    ...

```

### Examples

Shows how to number paragraphs using autonum fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Chaque champ AUTONUM affiche la valeur actuelle d'un compteur continu des champs AUTONUM,
# nous permettant de numéroter automatiquement les éléments comme une liste numérotée.
# Ce champ affichera le nombre "1.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 1.')
self.assertEqual(' AUTONUM ', field.get_field_code())
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 2.')
# Le caractère séparateur, qui apparaît dans le résultat du champ immédiatement après le nombre, est un point par défaut.
# Si nous laissons cette propriété à null, notre deuxième champ AUTONUM affichera "2." dans le document.
self.assertIsNone(field.separator_character)
# Nous pouvons définir cette propriété pour appliquer le premier caractère de sa chaîne comme nouveau caractère séparateur.
# Dans ce cas, notre champ AUTONUM affichera maintenant "2:".
field.separator_character = ':'
self.assertEqual(' AUTONUM  \\s :', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTONUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNum](../)

