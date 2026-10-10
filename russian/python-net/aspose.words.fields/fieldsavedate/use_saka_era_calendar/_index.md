---
title: FieldSaveDate.use_saka_era_calendar property
linktitle: use_saka_era_calendar property
articleTitle: use_saka_era_calendar property
second_title: Aspose.Words for Python
description: "FieldSaveDate.use_saka_era_calendar property. Gets or sets whether to use the Saka Era calendar."
type: docs
weight: 30
url: /ru/python-net/aspose.words.fields/fieldsavedate/use_saka_era_calendar/
---

## FieldSaveDate.use_saka_era_calendar property

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

Shows how to use the SAVEDATE field to display the date/time of the document's most recent save operation performed using Microsoft Word.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
builder = aw.DocumentBuilder(doc=doc)
builder.move_to_document_end()
builder.writeln(' Date this document was last saved:')
# Мы можем использовать поле SAVEDATE, чтобы отобразить дату и время последней операции сохранения в документе.
# Операция сохранения, к которой относятся эти поля, — это ручное сохранение в приложении, таком как Microsoft Word,
# а не метод Save документа.
# Ниже представлены три разных типа календаря, в соответствии с которыми поле SAVEDATE может отображать дату/время.
# 1 -  Исламский лунный календарь:
builder.write('According to the Lunar Calendar - ')
field = builder.insert_field(field_type=FieldType.FIELD_SAVE_DATE, update_field=True).as_field_save_date()
field.use_lunar_calendar = True
self.assertEqual(' SAVEDATE  \\h', field.get_field_code())
# 2 -  Календарь Умма аль-Кура:
builder.write('\nAccording to the Umm al-Qura calendar - ')
field = builder.insert_field(field_type=FieldType.FIELD_SAVE_DATE, update_field=True).as_field_save_date()
field.use_um_al_qura_calendar = True
self.assertEqual(' SAVEDATE  \\u', field.get_field_code())
# 3 -  Национальный индийский календарь:
builder.write('\nAccording to the Indian National calendar - ')
field = builder.insert_field(field_type=FieldType.FIELD_SAVE_DATE, update_field=True).as_field_save_date()
field.use_saka_era_calendar = True
self.assertEqual(' SAVEDATE  \\s', field.get_field_code())
# Поля SAVEDATE берут свои значения даты/времени из встроенного свойства LastSavedTime.
# Метод Save документа не обновит это значение, но мы всё равно можем обновить его вручную.
doc.built_in_document_properties.last_saved_time = datetime.datetime.now()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SAVEDATE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSaveDate](../)

