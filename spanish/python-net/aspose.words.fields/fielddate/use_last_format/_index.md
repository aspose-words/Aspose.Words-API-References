---
title: FieldDate.use_last_format property
linktitle: use_last_format property
articleTitle: use_last_format property
second_title: Aspose.Words for Python
description: "FieldDate.use_last_format property. Gets or sets whether to use a format last used by the hosting application when inserting a new DATE field."
type: docs
weight: 20
url: /es/python-net/aspose.words.fields/fielddate/use_last_format/
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
# Si queremos que el texto del documento siempre muestre la fecha correcta, podemos usar un campo DATE.
# A continuación se presentan tres tipos de calendarios culturales que un campo DATE puede usar para mostrar una fecha.
# 1 -  Calendario lunar islámico:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_lunar_calendar = True
self.assertEqual(' DATE  \\h', field.get_field_code())
builder.writeln()
# 2 -  Calendario Umm al-Qura:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_um_al_qura_calendar = True
self.assertEqual(' DATE  \\u', field.get_field_code())
builder.writeln()
# 3 -  Calendario nacional indio:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_saka_era_calendar = True
self.assertEqual(' DATE  \\s', field.get_field_code())
builder.writeln()
# Inserte un campo DATE y establezca su tipo de calendario al que se usó por última vez en la aplicación host.
# En Microsoft Word, el tipo será el más recientemente usado en el cuadro de diálogo Insertar -> Texto -> Fecha y hora.
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

