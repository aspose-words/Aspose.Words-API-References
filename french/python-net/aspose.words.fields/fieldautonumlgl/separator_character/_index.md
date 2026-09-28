---
title: FieldAutoNumLgl.separator_character property
linktitle: separator_character property
articleTitle: separator_character property
second_title: Aspose.Words for Python
description: "FieldAutoNumLgl.separator_character property. Gets or sets the separator character to be used."
type: docs
weight: 30
url: /fr/python-net/aspose.words.fields/fieldautonumlgl/separator_character/
---

## FieldAutoNumLgl.separator_character property

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

Shows how to organize a document using AUTONUMLGL fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
filler_text = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ' + '\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. '
# Les champs AUTONUMLGL affichent un nombre qui s'incrémente à chaque champ AUTONUMLGL au sein de son niveau de titre actuel.
# Ces champs maintiennent un compte séparé pour chaque niveau de titre,
# et chaque champ affiche également les comptes de champs AUTONUMLGL pour tous les niveaux de titre inférieurs au sien.
# Modifier le compteur pour n'importe quel niveau de titre réinitialise les compteurs de tous les niveaux supérieurs à 1.
# Cela nous permet d'organiser notre document sous forme de liste structurée.
# Ceci est le premier champ AUTONUMLGL à un niveau de titre de 1, affichant "1." dans le document.
ExField._insert_numbered_clause(builder, '\tHeading 1', filler_text, aw.StyleIdentifier.HEADING1)
# Ceci est le deuxième champ AUTONUMLGL à un niveau de titre de 1, il affichera donc "2.".
ExField._insert_numbered_clause(builder, '\tHeading 2', filler_text, aw.StyleIdentifier.HEADING1)
# Ceci est le premier champ AUTONUMLGL à un niveau de titre de 2,
# et le compteur AUTONUMLGL pour le niveau de titre inférieur est "2", il affichera donc "2.1.".
ExField._insert_numbered_clause(builder, '\tHeading 3', filler_text, aw.StyleIdentifier.HEADING2)
# Ceci est le premier champ AUTONUMLGL à un niveau de titre de 3.
# Fonctionnant de la même manière que le champ ci‑dessus, il affichera "2.1.1.".
ExField._insert_numbered_clause(builder, '\tHeading 4', filler_text, aw.StyleIdentifier.HEADING3)
# Ce champ est à un niveau de titre de 2, et son compteur AUTONUMLGL respectif est à 2, il affichera donc "2.2.".
ExField._insert_numbered_clause(builder, '\tHeading 5', filler_text, aw.StyleIdentifier.HEADING2)
# Incrémenter le compteur AUTONUMLGL pour un niveau de titre inférieur à celui‑ci
# a réinitialisé le compteur pour ce niveau afin que ce champ affiche "2.2.1.".
ExField._insert_numbered_clause(builder, '\tHeading 6', filler_text, aw.StyleIdentifier.HEADING3)
for field in list(filter(lambda f: f.type == aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL, list(doc.range.fields))):
    field = field.as_field_auto_num_lgl()
    # Le caractère séparateur, qui apparaît dans le résultat du champ immédiatement après le nombre,
    # est un point par défaut. Si nous laissons cette propriété nulle,
    # notre dernier champ AUTONUMLGL affichera "2.2.1." dans le document.
    self.assertIsNone(field.separator_character)
    # Définir un caractère séparateur personnalisé et supprimer le point final
    # modifiera l'apparence de ce champ de "2.2.1." à "2:2:1".
    # Nous appliquerons cela à tous les champs que nous avons créés.
    field.separator_character = ':'
    field.remove_trailing_period = True
    self.assertEqual(' AUTONUMLGL  \\s : \\e', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTONUMLGL.docx')
```

Shows how to organize a document using AUTONUMLGL fields (InsertNumberedClause).

```python
@staticmethod
def _insert_numbered_clause(builder, heading, contents, heading_style):
    builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL, update_field=True)
    builder.current_paragraph.paragraph_format.style_identifier = heading_style
    builder.writeln(heading)
    # Ce texte appartiendra au champ auto num legal qui le précède.
    # Il se réduira lorsque nous cliquerons sur la flèche à côté du champ AUTONUMLGL correspondant dans Microsoft Word.
    builder.current_paragraph.paragraph_format.style_identifier = aw.StyleIdentifier.BODY_TEXT
    builder.writeln(contents)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNumLgl](../)

