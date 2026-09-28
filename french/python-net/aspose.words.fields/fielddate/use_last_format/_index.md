---
title: FieldDate.use_last_format property
linktitle: use_last_format property
articleTitle: use_last_format property
second_title: Aspose.Words for Python
description: "FieldDate.use_last_format property. Gets or sets whether to use a format last used by the hosting application when inserting a new DATE field."
type: docs
weight: 20
url: /fr/python-net/aspose.words.fields/fielddate/use_last_format/
---

## FieldDate.use_last_format property

Gets or sets whether to use a format last used by the hosting application when inserting a new DATE field.


```python
@property
def use_last_format(self) -> bool:
    ...

@use_last_format.setter
def use_last_format(self, value: bool):
    ...

```

### Examples

Shows how to use DATE fields to display dates according to different kinds of calendars.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Si nous voulons que le texte du document affiche toujours la date correcte, nous pouvons utiliser un champ DATE.
# Voici trois types de calendriers culturels qu'un champ DATE peut utiliser pour afficher une date.
# 1 -  Calendrier lunaire islamique :
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_lunar_calendar = True
self.assertEqual(' DATE  \\h', field.get_field_code())
builder.writeln()
# 2 -  Calendrier Umm al-Qura :
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_um_al_qura_calendar = True
self.assertEqual(' DATE  \\u', field.get_field_code())
builder.writeln()
# 3 -  Calendrier national indien :
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_saka_era_calendar = True
self.assertEqual(' DATE  \\s', field.get_field_code())
builder.writeln()
# Insérez un champ DATE et définissez son type de calendrier sur celui utilisé en dernier par l'application hôte.
# Dans Microsoft Word, le type sera celui le plus récemment utilisé dans la boîte de dialogue Insertion -> Texte -> Date et heure.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_last_format = True
self.assertEqual(' DATE  \\l', field.get_field_code())
builder.writeln()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.DATE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldDate](../)

