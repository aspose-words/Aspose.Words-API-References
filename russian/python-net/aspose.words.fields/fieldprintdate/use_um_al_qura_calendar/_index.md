---
title: FieldPrintDate.use_um_al_qura_calendar property
linktitle: use_um_al_qura_calendar property
articleTitle: use_um_al_qura_calendar property
second_title: Aspose.Words for Python
description: "FieldPrintDate.use_um_al_qura_calendar property. Gets or sets whether to use the Um-al-Qura calendar."
type: docs
weight: 40
url: /ru/python-net/aspose.words.fields/fieldprintdate/use_um_al_qura_calendar/
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
# Когда документ печатается принтером или печатается как PDF (но не экспортируется в PDF),
# Поля PRINTDATE будут отображать дату/время операции печати.
# Если печать не происходила, эти поля будут отображать "0/0/0000".
field = doc.range.fields[0].as_field_print_date()
self.assertEqual('3/25/2020 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE ', field.get_field_code())
# Ниже представлены три разных типа календаря, в соответствии с которыми поле PRINTDATE
# может отображать дату и время последней операции печати.
# 1 -  Исламский лунный календарь:
field = doc.range.fields[1].as_field_print_date()
self.assertTrue(field.use_lunar_calendar)
self.assertEqual('8/1/1441 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\h', field.get_field_code())
field = doc.range.fields[2].as_field_print_date()
# 2 -  Календарь Умма аль-Кура:
self.assertTrue(field.use_um_al_qura_calendar)
self.assertEqual('8/1/1441 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\u', field.get_field_code())
field = doc.range.fields[3].as_field_print_date()
# 3 -  Индийский национальный календарь:
self.assertTrue(field.use_saka_era_calendar)
self.assertEqual('1/5/1942 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\s', field.get_field_code())
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldPrintDate](../)

