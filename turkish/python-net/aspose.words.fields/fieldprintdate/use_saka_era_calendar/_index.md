---
title: FieldPrintDate.use_saka_era_calendar property
linktitle: use_saka_era_calendar property
articleTitle: use_saka_era_calendar property
second_title: Aspose.Words for Python
description: "FieldPrintDate.use_saka_era_calendar property. Gets or sets whether to use the Saka Era calendar."
type: docs
weight: 30
url: /tr/python-net/aspose.words.fields/fieldprintdate/use_saka_era_calendar/
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
# Bir belge bir yazıcıyla yazdırıldığında veya PDF olarak yazdırıldığında (ancak PDF olarak dışa aktarılmadığında),
# PRINTDATE alanları, yazdırma işleminin tarih/saat bilgisini gösterecektir.
# Eğer hiçbir yazdırma gerçekleşmemişse, bu alanlar "0/0/0000" gösterecektir.
field = doc.range.fields[0].as_field_print_date()
self.assertEqual('3/25/2020 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE ', field.get_field_code())
# Aşağıda, PRINTDATE alanının göreceli olarak kullanabileceği üç farklı takvim türü bulunmaktadır.
# son yazdırma işleminin tarih ve saatini gösterebilir.
# 1 -  İslami Hicri Takvim:
field = doc.range.fields[1].as_field_print_date()
self.assertTrue(field.use_lunar_calendar)
self.assertEqual('8/1/1441 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\h', field.get_field_code())
field = doc.range.fields[2].as_field_print_date()
# 2 -  Umm al-Qura takvimi:
self.assertTrue(field.use_um_al_qura_calendar)
self.assertEqual('8/1/1441 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\u', field.get_field_code())
field = doc.range.fields[3].as_field_print_date()
# 3 -  Hindistan Ulusal Takvimi:
self.assertTrue(field.use_saka_era_calendar)
self.assertEqual('1/5/1942 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\s', field.get_field_code())
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldPrintDate](../)

