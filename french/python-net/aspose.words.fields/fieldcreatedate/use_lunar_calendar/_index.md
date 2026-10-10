---
title: FieldCreateDate.use_lunar_calendar property
linktitle: use_lunar_calendar property
articleTitle: use_lunar_calendar property
second_title: Aspose.Words for Python
description: "FieldCreateDate.use_lunar_calendar property. Gets or sets whether to use the Hijri Lunar or Hebrew Lunar calendar."
type: docs
weight: 20
url: /fr/python-net/aspose.words.fields/fieldcreatedate/use_lunar_calendar/
---

## FieldCreateDate.use_lunar_calendar property

Gets or sets whether to use the Hijri Lunar or Hebrew Lunar calendar.


```python
@property
def use_lunar_calendar(self) -> bool:
    ...

@use_lunar_calendar.setter
def use_lunar_calendar(self, value: bool):
    ...

```

### Examples

Shows how to use the CREATEDATE field to display the creation date/time of the document.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
builder = aw.DocumentBuilder(doc=doc)
builder.move_to_document_end()
builder.writeln(' Date this document was created:')
# Nous pouvons utiliser le champ CREATEDATE pour afficher la date et l'heure de la création du document.
# Ci-dessous se trouvent trois types de calendriers différents selon lesquels le champ CREATEDATE peut afficher la date/heure.
# 1 -  Calendrier lunaire islamique :
builder.write('According to the Lunar Calendar - ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_CREATE_DATE, update_field=True).as_field_create_date()
field.use_lunar_calendar = True
assert ' CREATEDATE  \\h' == field.get_field_code()
# 2 -  Calendrier Umm al-Qura :
builder.write('\nAccording to the Umm al-Qura Calendar - ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_CREATE_DATE, update_field=True).as_field_create_date()
field.use_um_al_qura_calendar = True
assert ' CREATEDATE  \\u' == field.get_field_code()
# 3 -  Calendrier national indien :
builder.write('\nAccording to the Indian National Calendar - ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_CREATE_DATE, update_field=True).as_field_create_date()
field.use_saka_era_calendar = True
assert ' CREATEDATE  \\s' == field.get_field_code()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.CREATEDATE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldCreateDate](../)

