---
title: use_um_al_qura_calendar property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets whether to use the Um-al-Qura calendar."
type: docs
weight: 50
url: /python-net/aspose.words.fields/fielddate/use_um_al_qura_calendar/
---

## FieldDate.use_um_al_qura_calendar property

Gets or sets whether to use the Um-al-Qura calendar.


### Examples

Shows how to use DATE fields to display dates according to different kinds of calendars.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# If we want the text in the document always to display the correct date, we can use a DATE field.
# Below are three types of cultural calendars that a DATE field can use to display a date.
# 1 -  Islamic Lunar Calendar:
field = builder.insert_field(aw.fields.FieldType.FIELD_DATE, True).as_field_date()
field.use_lunar_calendar = True
self.assertEqual(" DATE  \\h", field.get_field_code())
builder.writeln()

# 2 -  Umm al-Qura calendar:
field = builder.insert_field(aw.fields.FieldType.FIELD_DATE, True).as_field_date()
field.use_um_al_qura_calendar = True
self.assertEqual(" DATE  \\u", field.get_field_code())
builder.writeln()

# 3 -  Indian National Calendar:
field = builder.insert_field(aw.fields.FieldType.FIELD_DATE, True).as_field_date()
field.use_saka_era_calendar = True
self.assertEqual(" DATE  \\s", field.get_field_code())
builder.writeln()

# Insert a DATE field and set its calendar type to the one last used by the host application.
# In Microsoft Word, the type will be the most recently used in the Insert -> Text -> Date and Time dialog box.
field = builder.insert_field(aw.fields.FieldType.FIELD_DATE, True).as_field_date()
field.use_last_format = True
self.assertEqual(" DATE  \\l", field.get_field_code())
builder.writeln()

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_date.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldDate](../)

