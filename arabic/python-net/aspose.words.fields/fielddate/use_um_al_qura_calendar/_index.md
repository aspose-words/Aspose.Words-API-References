---
title: FieldDate.use_um_al_qura_calendar property
linktitle: use_um_al_qura_calendar property
articleTitle: use_um_al_qura_calendar property
second_title: Aspose.Words for Python
description: "FieldDate.use_um_al_qura_calendar property. Gets or sets whether to use the Um-al-Qura calendar."
type: docs
weight: 50
url: /ar/python-net/aspose.words.fields/fielddate/use_um_al_qura_calendar/
---

## FieldDate.use_um_al_qura_calendar property

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

Shows how to use DATE fields to display dates according to different kinds of calendars.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# إذا أردنا أن يظهر النص في المستند دائمًا التاريخ الصحيح، يمكننا استخدام حقل DATE.
# فيما يلي ثلاثة أنواع من التقويمات الثقافية التي يمكن لحقل DATE استخدامها لعرض تاريخ.
# 1 -  التقويم القمري الإسلامي:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_lunar_calendar = True
self.assertEqual(' DATE  \\h', field.get_field_code())
builder.writeln()
# 2 -  تقويم أم القرى:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_um_al_qura_calendar = True
self.assertEqual(' DATE  \\u', field.get_field_code())
builder.writeln()
# 3 -  التقويم الوطني الهندي:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_saka_era_calendar = True
self.assertEqual(' DATE  \\s', field.get_field_code())
builder.writeln()
# أدرج حقل DATE وحدد نوع تقويمه إلى النوع الذي استخدمه التطبيق المضيف آخر مرة.
# في Microsoft Word، سيكون النوع هو الأكثر استخدامًا مؤخرًا في مربع الحوار Insert -> Text -> Date and Time.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_last_format = True
self.assertEqual(' DATE  \\l', field.get_field_code())
builder.writeln()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.DATE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldDate](../)

