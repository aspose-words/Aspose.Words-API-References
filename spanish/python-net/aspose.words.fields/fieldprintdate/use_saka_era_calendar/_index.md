---
title: FieldPrintDate.use_saka_era_calendar property
linktitle: use_saka_era_calendar property
articleTitle: use_saka_era_calendar property
second_title: Aspose.Words for Python
description: "FieldPrintDate.use_saka_era_calendar property. Gets or sets whether to use the Saka Era calendar."
type: docs
weight: 30
url: /es/python-net/aspose.words.fields/fieldprintdate/use_saka_era_calendar/
---

## FieldPrintDate.use_saka_era_calendar property

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

Shows read PRINTDATE fields.

```python
doc = aw.Document(file_name=MY_DIR + 'Field sample - PRINTDATE.docx')
# Cuando un documento se imprime con una impresora o se imprime como PDF (pero no se exporta a PDF),
# Los campos PRINTDATE mostrarán la fecha/hora de la operación de impresión.
# Si no se ha realizado ninguna impresión, estos campos mostrarán "0/0/0000".
field = doc.range.fields[0].as_field_print_date()
self.assertEqual('3/25/2020 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE ', field.get_field_code())
# A continuación se presentan tres tipos de calendario diferentes según los cuales el campo PRINTDATE
# puede mostrar la fecha y hora de la última operación de impresión.
# 1 -  Calendario lunar islámico:
field = doc.range.fields[1].as_field_print_date()
self.assertTrue(field.use_lunar_calendar)
self.assertEqual('8/1/1441 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\h', field.get_field_code())
field = doc.range.fields[2].as_field_print_date()
# 2 -  Calendario Umm al-Qura:
self.assertTrue(field.use_um_al_qura_calendar)
self.assertEqual('8/1/1441 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\u', field.get_field_code())
field = doc.range.fields[3].as_field_print_date()
# 3 -  Calendario nacional indio:
self.assertTrue(field.use_saka_era_calendar)
self.assertEqual('1/5/1942 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\s', field.get_field_code())
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldPrintDate](../)

