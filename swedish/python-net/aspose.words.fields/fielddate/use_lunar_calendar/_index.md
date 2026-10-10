---
title: FieldDate.use_lunar_calendar property
linktitle: use_lunar_calendar property
articleTitle: use_lunar_calendar property
second_title: Aspose.Words for Python
description: "FieldDate.use_lunar_calendar property. Gets or sets whether to use the Hijri Lunar or Hebrew Lunar calendar."
type: docs
weight: 30
url: /sv/python-net/aspose.words.fields/fielddate/use_lunar_calendar/
---

## FieldDate.use_lunar_calendar property

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

Shows how to use DATE fields to display dates according to different kinds of calendars.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Om vi vill att texten i dokumentet alltid ska visa rätt datum, kan vi använda ett DATE-fält.
# Nedan följer tre typer av kulturella kalendrar som ett DATE-fält kan använda för att visa ett datum.
# 1 -  Islamisk månkalender:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_lunar_calendar = True
self.assertEqual(' DATE  \\h', field.get_field_code())
builder.writeln()
# 2 -  Umm al-Qura-kalender:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_um_al_qura_calendar = True
self.assertEqual(' DATE  \\u', field.get_field_code())
builder.writeln()
# 3 -  Indisk nationell kalender:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_saka_era_calendar = True
self.assertEqual(' DATE  \\s', field.get_field_code())
builder.writeln()
# Infoga ett DATE-fält och ställ in dess kalendertyp till den som senast användes av värdprogrammet.
# I Microsoft Word kommer typen att vara den senast använda i dialogrutan Infoga -> Text -> Datum och tid.
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

