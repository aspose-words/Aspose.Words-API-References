---
title: FieldDate.use_last_format property
linktitle: use_last_format property
articleTitle: use_last_format property
second_title: Aspose.Words for Python
description: "FieldDate.use_last_format property. Gets or sets whether to use a format last used by the hosting application when inserting a new DATE field."
type: docs
weight: 20
url: /tr/python-net/aspose.words.fields/fielddate/use_last_format/
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
# Belgedeki metnin her zaman doğru tarihi göstermesini istiyorsak, bir DATE alanı kullanabiliriz.
# Aşağıda, bir DATE alanının tarihi göstermek için kullanabileceği üç kültürel takvim türü bulunmaktadır.
# 1 -  İslami Hicri Takvim:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_lunar_calendar = True
self.assertEqual(' DATE  \\h', field.get_field_code())
builder.writeln()
# 2 -  Umm al-Qura takvimi:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_um_al_qura_calendar = True
self.assertEqual(' DATE  \\u', field.get_field_code())
builder.writeln()
# 3 -  Hindistan Ulusal Takvimi:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_saka_era_calendar = True
self.assertEqual(' DATE  \\s', field.get_field_code())
builder.writeln()
# Bir DATE alanı ekleyin ve takvim türünü, ana uygulama tarafından en son kullanılan olarak ayarlayın.
# Microsoft Word'de, tür Insert -> Text -> Date and Time iletişim kutusunda en son kullanılan olacaktır.
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

