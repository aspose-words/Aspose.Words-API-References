---
title: FieldPrintDate.use_lunar_calendar property
linktitle: use_lunar_calendar property
articleTitle: use_lunar_calendar property
second_title: Aspose.Words for Python
description: "FieldPrintDate.use_lunar_calendar property. Gets or sets whether to use the Hijri Lunar or Hebrew Lunar calendar."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldprintdate/use_lunar_calendar/
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
# When a document is printed by a printer or printed as a PDF (but not exported to PDF),
# PRINTDATE fields will display the print operation's date/time.
# If no printing has taken place, these fields will display "0/0/0000".
field = doc.range.fields[0].as_field_print_date()
self.assertEqual('3/25/2020 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE ', field.get_field_code())
# Below are three different calendar types according to which the PRINTDATE field
# can display the date and time of the last printing operation.
# 1 -  Islamic Lunar Calendar:
field = doc.range.fields[1].as_field_print_date()
self.assertTrue(field.use_lunar_calendar)
self.assertEqual('8/1/1441 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\h', field.get_field_code())
field = doc.range.fields[2].as_field_print_date()
# 2 -  Umm al-Qura calendar:
self.assertTrue(field.use_um_al_qura_calendar)
self.assertEqual('8/1/1441 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\u', field.get_field_code())
field = doc.range.fields[3].as_field_print_date()
# 3 -  Indian National Calendar:
self.assertTrue(field.use_saka_era_calendar)
self.assertEqual('1/5/1942 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\s', field.get_field_code())
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldPrintDate](../)

