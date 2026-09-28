---
title: FieldPrintDate.use_saka_era_calendar property
linktitle: use_saka_era_calendar property
articleTitle: use_saka_era_calendar property
second_title: Aspose.Words for Python
description: "FieldPrintDate.use_saka_era_calendar property. Gets or sets whether to use the Saka Era calendar."
type: docs
weight: 30
url: /zh/python-net/aspose.words.fields/fieldprintdate/use_saka_era_calendar/
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
# 当文档通过打印机打印或以 PDF 形式打印时（但不是导出为 PDF），
# PRINTDATE 字段将显示打印操作的日期/时间。
# 如果没有进行打印，这些字段将显示 "0/0/0000"。
field = doc.range.fields[0].as_field_print_date()
self.assertEqual('3/25/2020 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE ', field.get_field_code())
# 以下是三种不同的日历类型，根据这些类型，PRINTDATE 字段
# 可以显示最近一次打印操作的日期和时间。
# 1 - 伊斯兰阴历：
field = doc.range.fields[1].as_field_print_date()
self.assertTrue(field.use_lunar_calendar)
self.assertEqual('8/1/1441 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\h', field.get_field_code())
field = doc.range.fields[2].as_field_print_date()
# 2 - 乌姆阿尔库拉历：
self.assertTrue(field.use_um_al_qura_calendar)
self.assertEqual('8/1/1441 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\u', field.get_field_code())
field = doc.range.fields[3].as_field_print_date()
# 3 - 印度国家历：
self.assertTrue(field.use_saka_era_calendar)
self.assertEqual('1/5/1942 12:00:00 AM', field.result)
self.assertEqual(' PRINTDATE  \\s', field.get_field_code())
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldPrintDate](../)

