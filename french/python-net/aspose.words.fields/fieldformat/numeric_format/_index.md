---
title: FieldFormat.numeric_format property
linktitle: numeric_format property
articleTitle: numeric_format property
second_title: Aspose.Words for Python
description: "FieldFormat.numeric_format property. Gets or sets a formatting that is applied to a numeric field result"
type: docs
weight: 30
url: /fr/python-net/aspose.words.fields/fieldformat/numeric_format/
---

## FieldFormat.numeric_format property

Gets or sets a formatting that is applied to a numeric field result. Corresponds to the \\# switch.


```python
@property
def numeric_format(self) -> str:
    ...

@numeric_format.setter
def numeric_format(self, value: str):
    ...

```

### Examples

Shows how to format field results.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Utilisez un constructeur de document pour insérer un champ qui affiche un résultat sans aucun format appliqué.
field = builder.insert_field(field_code='= 2 + 3')
self.assertEqual('= 2 + 3', field.get_field_code())
self.assertEqual('5', field.result)
# Nous pouvons appliquer un format au résultat d'un champ en utilisant les propriétés du champ.
# Voici trois types de formats que nous pouvons appliquer au résultat d'un champ.
# 1 -  Format numérique :
format_obj = field.format
format_obj.numeric_format = '$###.00'
field.update()
self.assertEqual('= 2 + 3 \\# $###.00', field.get_field_code())
self.assertEqual('$  5.00', field.result)
# 2 -  Format date/heure :
field = builder.insert_field(field_code='DATE')
format_obj = field.format
format_obj.date_time_format = 'dddd, MMMM dd, yyyy'
field.update()
self.assertEqual('DATE \\@ "dddd, MMMM dd, yyyy"', field.get_field_code())
print(f"Today's date, in {format_obj.date_time_format} format:\n\t{field.result}")
# 3 -  Format général :
field = builder.insert_field(field_code='= 25 + 33')
format_obj = field.format
format_obj.general_formats.add(aw.fields.GeneralFormat.LOWERCASE_ROMAN)
format_obj.general_formats.add(aw.fields.GeneralFormat.UPPER)
field.update()
index = 0
for general_format in format_obj.general_formats:
    print(f'General format index {index}: {general_format}')
    index += 1
self.assertEqual('= 25 + 33 \\* roman \\* Upper', field.get_field_code())
self.assertEqual('LVIII', field.result)
self.assertEqual(2, len(format_obj.general_formats))
self.assertEqual(aw.fields.GeneralFormat.LOWERCASE_ROMAN, format_obj.general_formats[0])
# Nous pouvons supprimer nos formats pour ramener le résultat du champ à sa forme originale.
format_obj.general_formats.remove(aw.fields.GeneralFormat.LOWERCASE_ROMAN)
format_obj.general_formats.remove_at(0)
self.assertEqual(0, len(format_obj.general_formats))
field.update()
self.assertEqual('= 25 + 33  ', field.get_field_code())
self.assertEqual('58', field.result)
self.assertEqual(0, len(format_obj.general_formats))
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldFormat](../)

