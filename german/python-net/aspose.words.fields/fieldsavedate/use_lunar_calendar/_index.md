---
title: FieldSaveDate.use_lunar_calendar property
linktitle: use_lunar_calendar property
articleTitle: use_lunar_calendar property
second_title: Aspose.Words for Python
description: "FieldSaveDate.use_lunar_calendar property. Gets or sets whether to use the Hijri Lunar or Hebrew Lunar calendar."
type: docs
weight: 20
url: /de/python-net/aspose.words.fields/fieldsavedate/use_lunar_calendar/
---

## FieldSaveDate.use_lunar_calendar property

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

Shows how to use the SAVEDATE field to display the date/time of the document's most recent save operation performed using Microsoft Word.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
builder = aw.DocumentBuilder(doc=doc)
builder.move_to_document_end()
builder.writeln(' Date this document was last saved:')
# Wir können das SAVEDATE-Feld verwenden, um das Datum und die Uhrzeit der letzten Speicheroperation im Dokument anzuzeigen.
# Die Speicheroperation, auf die sich diese Felder beziehen, ist das manuelle Speichern in einer Anwendung wie Microsoft Word,
# nicht die Save-Methode des Dokuments.
# Nachfolgend sind drei verschiedene Kalendertypen aufgeführt, nach denen das SAVEDATE-Feld Datum/Uhrzeit anzeigen kann.
# 1 -  Islamischer Mondkalender:
builder.write('According to the Lunar Calendar - ')
field = builder.insert_field(field_type=FieldType.FIELD_SAVE_DATE, update_field=True).as_field_save_date()
field.use_lunar_calendar = True
self.assertEqual(' SAVEDATE  \\h', field.get_field_code())
# 2 -  Umm al-Qura-Kalender:
builder.write('\nAccording to the Umm al-Qura calendar - ')
field = builder.insert_field(field_type=FieldType.FIELD_SAVE_DATE, update_field=True).as_field_save_date()
field.use_um_al_qura_calendar = True
self.assertEqual(' SAVEDATE  \\u', field.get_field_code())
# 3 -  Indischer Nationalkalender:
builder.write('\nAccording to the Indian National calendar - ')
field = builder.insert_field(field_type=FieldType.FIELD_SAVE_DATE, update_field=True).as_field_save_date()
field.use_saka_era_calendar = True
self.assertEqual(' SAVEDATE  \\s', field.get_field_code())
# Die SAVEDATE-Felder beziehen ihre Datums-/Uhrzeitwerte aus der integrierten Eigenschaft LastSavedTime.
# Die Save-Methode des Dokuments aktualisiert diesen Wert nicht, aber wir können ihn trotzdem manuell aktualisieren.
doc.built_in_document_properties.last_saved_time = datetime.datetime.now()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SAVEDATE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSaveDate](../)

