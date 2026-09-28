---
title: BuiltInDocumentProperties.last_saved_time property
linktitle: last_saved_time property
articleTitle: last_saved_time property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.last_saved_time property. Gets or sets the time of the last save in UTC."
type: docs
weight: 180
url: /ar/python-net/aspose.words.properties/builtindocumentproperties/last_saved_time/
---

## BuiltInDocumentProperties.last_saved_time property

Gets or sets the time of the last save in UTC.


```python
@property
def last_saved_time(self) -> datetime.datetime:
    ...

@last_saved_time.setter
def last_saved_time(self, value: datetime.datetime):
    ...

```

### Remarks

For documents originated from RTF format this property returns the local time of last save operation.

Aspose.Words does not update this property.




### Examples

Shows how to use the SAVEDATE field to display the date/time of the document's most recent save operation performed using Microsoft Word.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
builder = aw.DocumentBuilder(doc=doc)
builder.move_to_document_end()
builder.writeln(' Date this document was last saved:')
# يمكننا استخدام حقل SAVEDATE لعرض تاريخ ووقت عملية الحفظ الأخيرة في المستند.
# عملية الحفظ التي تشير إليها هذه الحقول هي الحفظ اليدوي في تطبيق مثل Microsoft Word،
# وليس طريقة Save الخاصة بالمستند.
# فيما يلي ثلاثة أنواع مختلفة من التقويمات التي يمكن لحقل SAVEDATE من خلالها عرض التاريخ/الوقت.
# 1 -  التقويم القمري الإسلامي:
builder.write('According to the Lunar Calendar - ')
field = builder.insert_field(field_type=FieldType.FIELD_SAVE_DATE, update_field=True).as_field_save_date()
field.use_lunar_calendar = True
self.assertEqual(' SAVEDATE  \\h', field.get_field_code())
# 2 -  تقويم أم القرى:
builder.write('\nAccording to the Umm al-Qura calendar - ')
field = builder.insert_field(field_type=FieldType.FIELD_SAVE_DATE, update_field=True).as_field_save_date()
field.use_um_al_qura_calendar = True
self.assertEqual(' SAVEDATE  \\u', field.get_field_code())
# 3 -  التقويم الوطني الهندي:
builder.write('\nAccording to the Indian National calendar - ')
field = builder.insert_field(field_type=FieldType.FIELD_SAVE_DATE, update_field=True).as_field_save_date()
field.use_saka_era_calendar = True
self.assertEqual(' SAVEDATE  \\s', field.get_field_code())
# حقول SAVEDATE تستمد قيم التاريخ/الوقت الخاصة بها من الخاصية المدمجة LastSavedTime.
# طريقة Save الخاصة بالمستند لن تقوم بتحديث هذه القيمة، لكن لا يزال بإمكاننا تحديثها يدويًا.
doc.built_in_document_properties.last_saved_time = datetime.datetime.now()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SAVEDATE.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

