---
title: FieldDate.use_saka_era_calendar property
linktitle: use_saka_era_calendar property
articleTitle: use_saka_era_calendar property
second_title: Aspose.Words for Python
description: "FieldDate.use_saka_era_calendar property. Gets or sets whether to use the Saka Era calendar."
type: docs
weight: 40
url: /ru/python-net/aspose.words.fields/fielddate/use_saka_era_calendar/
---

## FieldDate.use_saka_era_calendar property

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

Shows how to use DATE fields to display dates according to different kinds of calendars.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Если мы хотим, чтобы текст в документе всегда отображал правильную дату, мы можем использовать поле DATE.
# Ниже представлены три типа культурных календарей, которые поле DATE может использовать для отображения даты.
# 1 -  Исламский лунный календарь:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_lunar_calendar = True
self.assertEqual(' DATE  \\h', field.get_field_code())
builder.writeln()
# 2 -  Календарь Умма аль-Кура:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_um_al_qura_calendar = True
self.assertEqual(' DATE  \\u', field.get_field_code())
builder.writeln()
# 3 -  Индийский национальный календарь:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.use_saka_era_calendar = True
self.assertEqual(' DATE  \\s', field.get_field_code())
builder.writeln()
# Вставьте поле DATE и установите тип календаря в тот, который последний раз использовалось хост‑приложением.
# В Microsoft Word тип будет тем, который использовался последним в диалоговом окне Вставка -> Текст -> Дата и время.
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

