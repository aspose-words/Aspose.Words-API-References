---
title: FieldSaveDate.use_saka_era_calendar property
linktitle: use_saka_era_calendar property
articleTitle: use_saka_era_calendar property
second_title: Aspose.Words for Python
description: "FieldSaveDate.use_saka_era_calendar property. Gets or sets whether to use the Saka Era calendar."
type: docs
weight: 30
url: /python-net/aspose.words.fields/fieldsavedate/use_saka_era_calendar/
---

## FieldSaveDate.use_saka_era_calendar property

Gets or sets whether to use the Saka Era calendar.


```python
@property
def use_saka_era_calendar(self) -> bool:
    ...

@use_saka_era_calendar.setter
def use_saka_era_calendar(self, value: bool):
    ...

```

### Examples

Shows how to use the SAVEDATE field to display the date/time of the document's most recent save operation performed using Microsoft Word.

```python
doc = aw.Document(MY_DIR + 'Document.docx')
builder = aw.DocumentBuilder(doc)
builder.move_to_document_end()
builder.writeln(' Date this document was last saved:')
# We can use the SAVEDATE field to display the last save operation's date and time on the document.
# The save operation that these fields refer to is the manual save in an application like Microsoft Word,
# not the document's "save" method.
# Below are three different calendar types according to which the SAVEDATE field can display the date/time.
# 1 -  Islamic Lunar Calendar:
builder.write('According to the Lunar Calendar - ')
field = builder.insert_field(aw.fields.FieldType.FIELD_SAVE_DATE, True).as_field_save_date()
field.use_lunar_calendar = True
self.assertEqual(' SAVEDATE  \\h', field.get_field_code())
# 2 -  Umm al-Qura calendar:
builder.write('\nAccording to the Umm al-Qura calendar - ')
field = builder.insert_field(aw.fields.FieldType.FIELD_SAVE_DATE, True).as_field_save_date()
field.use_um_al_qura_calendar = True
self.assertEqual(' SAVEDATE  \\u', field.get_field_code())
# 3 -  Indian National calendar:
builder.write('\nAccording to the Indian National calendar - ')
field = builder.insert_field(aw.fields.FieldType.FIELD_SAVE_DATE, True).as_field_save_date()
field.use_saka_era_calendar = True
self.assertEqual(' SAVEDATE  \\s', field.get_field_code())
# The SAVEDATE fields draw their date/time values from the "last_saved_time" built-in property.
# The document's Save method will not update this value, but we can still update it manually.
doc.built_in_document_properties.last_saved_time = datetime.datetime.now()
doc.update_fields()
doc.save(ARTIFACTS_DIR + 'Field.field_save_date.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSaveDate](../)

