---
title: FieldPrintDate.use_um_al_qura_calendar property
linktitle: use_um_al_qura_calendar property
articleTitle: use_um_al_qura_calendar property
second_title: Aspose.Words for Python
description: "FieldPrintDate.use_um_al_qura_calendar property. Gets or sets whether to use the Um-al-Qura calendar."
type: docs
weight: 40
url: /fr/python-net/aspose.words.fields/fieldprintdate/use_um_al_qura_calendar/
---

## FieldPrintDate.use_um_al_qura_calendar property

Gets or sets whether to use the Um-al-Qura calendar.


```python
@property
def use_um_al_qura_calendar(self) -> bool:
    ...

@use_um_al_qura_calendar.setter
def use_um_al_qura_calendar(self, value: bool):
    ...

```

### Examples

Shows read PRINTDATE fields.

```python
doc = aw.Document(file_name=MY_DIR + 'Field sample - PRINTDATE.docx')
# Lorsqu'un document est imprimé par une imprimante ou imprimé en PDF (mais pas exporté en PDF),
# Les champs PRINTDATE afficheront la date/heure de l'opération d'impression.
# Si aucune impression n'a eu lieu, ces champs afficheront "0/0/0000".
field = doc.range.fields[0].as_field_print_date()
self.assertEqual('3/25/2020 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE ', field.get_field_code())
# Ci-dessous, trois types de calendrier différents selon lesquels le champ PRINTDATE
# peut afficher la date et l'heure de la dernière opération d'impression.
# 1 -  Calendrier lunaire islamique :
field = doc.range.fields[1].as_field_print_date()
self.assertTrue(field.use_lunar_calendar)
self.assertEqual('8/1/1441 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\h', field.get_field_code())
field = doc.range.fields[2].as_field_print_date()
# 2 -  Calendrier Umm al-Qura :
self.assertTrue(field.use_um_al_qura_calendar)
self.assertEqual('8/1/1441 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\u', field.get_field_code())
field = doc.range.fields[3].as_field_print_date()
# 3 -  Calendrier national indien :
self.assertTrue(field.use_saka_era_calendar)
self.assertEqual('1/5/1942 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\s', field.get_field_code())
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldPrintDate](../)

