---
title: FieldPrintDate.use_lunar_calendar property
linktitle: use_lunar_calendar property
articleTitle: use_lunar_calendar property
second_title: Aspose.Words for Python
description: "FieldPrintDate.use_lunar_calendar property. Gets or sets whether to use the Hijri Lunar or Hebrew Lunar calendar."
type: docs
weight: 20
url: /de/python-net/aspose.words.fields/fieldprintdate/use_lunar_calendar/
---

## FieldPrintDate.use_lunar_calendar property

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

Shows read PRINTDATE fields.

```python
doc = aw.Document(file_name=MY_DIR + 'Field sample - PRINTDATE.docx')
# Wenn ein Dokument von einem Drucker ausgedruckt oder als PDF gedruckt wird (aber nicht als PDF exportiert wird),
# PRINTDATE-Felder zeigen das Datum/Uhrzeit des Druckvorgangs an.
# Wenn kein Druck stattgefunden hat, zeigen diese Felder "0/0/0000" an.
field = doc.range.fields[0].as_field_print_date()
self.assertEqual('3/25/2020 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE ', field.get_field_code())
# Nachfolgend sind drei verschiedene Kalendertypen aufgeführt, nach denen das PRINTDATE-Feld
# das Datum und die Uhrzeit des letzten Druckvorgangs anzeigen kann.
# 1 -  Islamischer Mondkalender:
field = doc.range.fields[1].as_field_print_date()
self.assertTrue(field.use_lunar_calendar)
self.assertEqual('8/1/1441 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\h', field.get_field_code())
field = doc.range.fields[2].as_field_print_date()
# 2 -  Umm al-Qura-Kalender:
self.assertTrue(field.use_um_al_qura_calendar)
self.assertEqual('8/1/1441 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\u', field.get_field_code())
field = doc.range.fields[3].as_field_print_date()
# 3 -  Indischer Nationalkalender:
self.assertTrue(field.use_saka_era_calendar)
self.assertEqual('1/5/1942 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\s', field.get_field_code())
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldPrintDate](../)

